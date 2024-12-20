Пояснения к схемам, приведены только относительно неочевидных моментов

## 1. Работа с ботом.##
```
class InitInput(BaseModel):

    token: Optional[str] = Field(None,)

    user_id: int = Field(..., min_length=ID_LEN_MIN, max_length=ID_LEN_MAX)

    link: str = Field(..., min_length=LINK_LEN_MIN, max_length=LINK_LEN_MAX)

  
  

class InitOutput(BaseModel):

    message: str = Field(...,)

    error: Optional[str] = Field(None,)

    status_code: Optional[int] = Field(None,)



class FinalOutput(BaseModel):

    user_id: int = Field(..., ge=ID_LEN_MIN, le=ID_LEN_MAX)

    message: str = Field(...,)

    error: Optional[str] = Field(None,)
```

token - произвольный набор символов, заранее одинаковый для бота и апи, нужен для блокирования отправки запроса третьей стороной

## 2. Работа с AI.
```
class Send_to_ai(BaseModel):

    req_id: int = Field(...,)

    link: str = Field(...,)

  
  

class Got_from_ai(BaseModel):

    req_id: int = Field(...,)

    message: str = Field(...,)

    error: Optional[str] = Field(None,)



class API_Response(BaseModel):

    msg_status: str = Field(...,)
```

req_id - уникальный номер реквеста, 64 бита, используется для идентификации запроса и адресного ответа