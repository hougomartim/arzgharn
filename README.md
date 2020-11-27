```json
[
  {
    "register_status":{
      "1": {
        "codemelli": "string",
        "fullname": "fullname",
        "birth_date": "timestamp",
        "father_name": "string"
      },
      "2":{
        "shaba": "string",
        "bank_card": "string"
      },
      "3":"register completed"
    }
  },
  {
    "url": "application/receive_mobile/",
    "body": {
      "type": "object",
      "method": "post",
      "data": {
        "username": "string"
      },
      "response": {
        "message": "code send to the {}"
      }
    }
  },
  {
    "url": "application/mobile_verification/",
    "body": {
      "type": "object",
      "method": "post",
      "data": {
        "username": "string",
        "code": "string"
      },
      "response": {
        "message": [
          "username or code, incorrect",
          {
            "token":"string",
            "register_status":"integer"
          }
        ]
      }
    }
  },
  {
    "url": "application/signup_human_information/",
    "body": {
      "type": "object",
      "permission": "IsAuthenticated",
      "method": "post",
      "data": {
        "codemelli": "string",
        "fullname": "fullname",
        "birth_date": "timestamp",
        "father_name": "string"
      },
      "response": {
        "message": [
          "Excesption 001: {}",
          {
            "message":"success",
            "register_status":"integer"
          }
        ]
      }
    }
  },
  {
    "url": "application/validate_shaba_number/",
    "body": {
      "type": "object",
      "permission": "IsAuthenticated",
      "method": "post",
      "data": {
        "shaba": "string"
      },
      "response": {
        "message": [
          {
            "result":"bool"
          }
        ]
      }
    }
  },
  {
    "url": "application/validate_bank_card/",
    "body": {
      "type": "object",
      "permission": "IsAuthenticated",
      "method": "post",
      "data": {
        "bank_card": "string"
      },
      "response": {
        "message": [
          {
            "result":"bool"
          }
        ]
      }
    }
  },
  {
    "url": "application/signup_credit_information/",
    "body": {
      "type": "object",
      "permission": "IsAuthenticated",
      "method": "post",
      "data": {
        "shaba": "string",
        "bank_card": "string"
      },
      "response": {
        "message": [
          {
            "message":"string",
            "register_status": "integer"
          }
        ]
      }
    }
  },
  {
    "url": "application/user_information/",
    "body": {
      "type": "object",
      "permission": "IsAuthenticated",
      "method": "get",
      "response": "user profile json"
    }
  },
  {
    "url": "application/user_invoices/",
    "body": {
      "type": "list",
      "permission": "IsAuthenticated",
      "method": "get",
      "response": "user invoices json"
    }
  }
]
```
