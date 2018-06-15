错误码表
========


全局
-------

::

    [{
      "code": 200,
      "name": "Status200OK",
      "description": "ok"
    },
    {
      "code": 422,
      "name": "UnprocessableEntity",
      "description": "请求实体错误"
    },{
      "code": 417,
      "name": "ExpectationFailed",
      "description": "服务器内部错误"
    },
    {
      "code": 404,
      "name": "NotFound",
      "description": "未找到内容"
    }]

流量卡
-------

::

    [{
      "code": 10000,
      "name": "Transfer_ConsigneeIsNotExists",
      "description": "接收人账户不存在"
    }, {
      "code": 10001,
      "name": "Transfer_CardIDCanNotBeLessThanOne",
      "description": "卡号不能少于1个"
    }, {
      "code": 10002,
      "name": "Generate_ExptimeNeedGreaterThanNow",
      "description": "到期时间必须大于当前时间"
    }, {
      "code": 10003,
      "name": "Generate_MaximumOf99999999CardsPerDay",
      "description": "每天最多生成99,999,999张卡"
    }]

充值卡
-------

::

    [{
      "code": 10000,
      "name": "Transfer_ConsigneeIsNotExists",
      "description": "接收人账户不存在"
    }, {
      "code": 10001,
      "name": "Transfer_CardIDCanNotBeLessThanOne",
      "description": "卡号不能少于1个"
    }, {
      "code": 10002,
      "name": "Generate_ExptimeNeedGreaterThanNow",
      "description": "到期时间必须大于当前时间"
    }, {
      "code": 10003,
      "name": "Generate_MaximumOf99999999CardsPerDay",
      "description": "每天最多生成99,999,999张卡"
    }]