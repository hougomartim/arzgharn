```json
[
  {
    "register_status": {
      "0":{
        "password":"string",
        "password2": "string"
      },
      "1": {
        "codemelli": "string",
        "fullname": "fullname",
        "birth_date": "timestamp",
        "father_name": "string",
        "image": "image"
      },
      "2": {
        "shaba": "string",
        "bank_card": "string"
      },
      "3": "register completed"
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
  },
  {
    "url": "application/signup_mobile_verification/",
    "body": {
      "type": "object",
      "method": "post",
      "data": {
        "username": "string",
        "code": "string optional"
      },
      "response": {
        "message": "multiple message"
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
            "token": "string",
            "register_status": "integer"
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
        "father_name": "string",
        "image": "image"
      },
      "response": {
        "message": [
          "Excesption 001: {}",
          {
            "message": "success",
            "register_status": "integer"
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
            "result": "bool"
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
            "result": "bool"
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
            "message": "string",
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
  },
  {
    "url": "application/get_information/",
    "body": {
      "type": "object",
      "data": {
        "name": "string"
      },
      "permission": "",
      "method": "post",
      "response": ""
    }
  },
  {
    "url": "application/get_price_by_usd/",
    "body": {
      "type": "object",
      "data": {
        "name": "string"
      },
      "permission": "",
      "method": "post",
      "response": ""
    }
  },
  {
    "url": "application/get_full_information_realtime/",
    "body": {
      "type": "object",
      "data": {
        "name": "string"
      },
      "permission": "",
      "method": "post",
      "response": ""
    }
  },
  {
    "url": "application/get_full_information_from_db/",
    "body": {
      "type": "object",
      "data": {
        "name": "string"
      },
      "permission": "",
      "method": "post",
      "response": ""
    }
  },
  {
    "url": "application/create_wallet/",
    "body": {
      "type": "object",
      "data": {
        "currency_id": "integer",
        "name": "string",
        "address": "string"
      },
      "permission": "IsAuthenticated",
      "method": "post",
      "response": "success"
    }
  },
  {
    "url": "application/delete_wallet/",
    "body": {
      "type": "object",
      "data": {
        "wallet_id": "integer"
      },
      "permission": "IsAuthenticated",
      "method": "post",
      "response": "success"
    }
  },
  {
    "url": "application/create_invoice/",
    "body": {
      "type": "object",
      "data": {
        "amount": "integer",
        "type": "kharid or forosh",
        "currency_id": "integer",
        "wallet_id": "integer",
        "transaction_id": "string"
      },
      "permission": "IsAuthenticated",
      "method": "post",
      "response": ""
    }
  },
  {
    "url": "application/list_currency/",
    "permission": "",
    "method": "get",
    "response": "list"
  },
  {
    "url": "application/show_wallets/",
    "permission": "",
    "method": "get",
    "response": "list"
  },
  {
    "url": "application/show_wallets/?currency_id={id}",
    "permission": "",
    "method": "get",
    "response": "list"
  },
  {
    "url": "admincp/invoices/",
    "permission": "IsSuperUser",
    "method": "get",
    "response": "list"
  },
  },
  {
    "url": "admincp/admin/",
    "description": "list superusers"
    "permission": "IsSuperUser",
    "method": "get",
    "response": "list"
  },
  {
    "url": "admincp/invoices/",
    "body": {
      "type": "object",
      "data": {
        "status": "integer",
        "invoice_id": "integer"
      },
      "permission": "IsSuperUser",
      "method": "post",
      "description": "change status",
      "response": ""
    }
  }
  },
  {
    "url": "admincp/admin/",
    "body": {
      "type": "object",
      "data": {
        "username": "string",
        "first_name": "string",
        "last_name": "string",
        "email": "string",
      },
      "permission": "IsSuperUser",
      "method": "post",
      "description": "change status",
      "response": ""
    }
  },
  {
    "url": "admincp/users/",
    "description": "list users"
    "permission": "IsSuperUser",
    "method": "get",
    "response": "list"
  },
  {
    "url": "admincp/users/",
    "body": {
      "type": "object",
      "data": {
        "profile_id": "integer",
        "status": "integer"
      },
      "permission": "IsSuperUser",
      "method": "post",
      "description": "change register_status",
      "response": ""
    }
  },
  {
    "url": "admincp/currency/",
    "description": "list currencies"
    "permission": "IsSuperUser",
    "method": "get",
    "response": "list"
  },
  {
    "url": "admincp/currency/",
    "body": {
      "type": "object",
      "data": {
        "currency_id": "integer",
        "fee": "integer",
        "minimum_trade_amount_by_toman": "integer",
        "maximum_trade_amount_by_toman": "integer",
        "trade_status": "integer",
        "admin_wallet_address": "string"
      },
      "permission": "IsSuperUser",
      "method": "post",
      "description": "change register_status",
      "response": ""
    }
  }
  },
  {
    "url": "application/add_password/",
    "body": {
      "type": "object",
      "data": {
        "password": "string",
        "password2": "string"
      },
      "permission": "IsAuthenticated",
      "method": "post",
      "description": "change password",
      "response": "success"
    }
  }
  },
  {
    "url": "application/signup_mobile_verification/",
    "body": {
      "type": "object",
      "data": {
        "username": "string required",
        "code": "string optional"
      },
      "permission": "AllowAny",
      "method": "post",
      "description": "use in signup page",
      "response": ""
    }
  }
]

```
