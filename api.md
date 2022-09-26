### 罗列搜集到的api

前置需要cookie

查看米游社账户下绑定的原神游戏角色
GET
https://api-takumi.mihoyo.com/binding/api/getUserGameRolesByCookieToken

米游社账号信息
GET
https://bbs-api.mihoyo.com/user/wapi/getUserFullInfo?gids=2

客服记录查询原因
GET
https://webstatic.mihoyo.com/admin/mi18n/hk4e_global/m02251421001311/m02251421001311-zh-cn.json

客服记录查询
GET
https://hk4e-api.mihoyo.com/ysulog/api/getPrimogemLog?selfquery_type=1&lang=zh-cn&sign_type=2&auth_appid=csc&authkey_ver=1&authkey="账户的authkey从米游社断网获取"&game_biz=hk4e_cn&app_client=bbs&type=1&size=20&end_id=
注:end_id为空从头部查询，最大20条记录，迭代查询，最多6月，记录延迟1小时

角色首页宝箱
GET
https://api-takumi-record.mihoyo.com/game_record/app/genshin/api/index?role_id=uid&server=region

深渊记录
GET
https://api-takumi-record.mihoyo.com/game_record/app/genshin/api/spiralAbyss?role_id=uid&schedule_type=schedule_type&server=region

账户角色列表
POST
https://api-takumi-record.mihoyo.com/game_record/app/genshin/api/character
body: { role_id: uid, server: region }

实时便笺
GET
https://api-takumi.mihoyo.com/event/e20200928calculate/v1/sync/avatar/detail?role_id=uid&server=region

札记
GET
https://hk4e-api.mihoyo.com/event/ys_ledger/monthInfo?month=month&bind_uid=uid&bind_region=region

角色养成计算器
POST
https://api-takumi.mihoyo.com/event/e20200928calculate/v2/compute
body: 角色数据

角色天赋等级圣遗物等信息
GET
https://api-takumi.mihoyo.com/event/e20200928calculate/v1/sync/avatar/detail?uid=uid&region=region&avatar_id=avatar_id

角色技能列表
GET
https://api-takumi.mihoyo.com/event/e20200928calculate/v1/avatarSkill/list?avatar_id=avatar_id

前置无需cookie

当前卡池信息
GET
https://api-takumi.mihoyo.com/common/blackboard/ys_obc/v1/gacha_pool?app_sn=ys_obc

米游社banner推荐
GET
https://bbs-api.mihoyo.com/post/wapi/getOfficialRecommendedPosts?gids=2

米游社图鉴
GET
https://api-static.mihoyo.com/common/blackboard/ys_obc/v1/home/content/list?app_sn=ys_obc&channel_id=189

图鉴内容
GET
https://api-static.mihoyo.com/common/blackboard/ys_obc/v1/content/info?app_sn=ys_obc&content_id=4736
注:content_id从上个API的结果中获取

米游社banner推荐
GET
https://bbs-api.mihoyo.com/post/wapi/getOfficialRecommendedPosts?gids=2

获取公告
GET
https://bbs-api.mihoyo.com/post/wapi/getNewsList?gids=2&page_size=20&type=1
注:type=1为公告，2、3为活动资讯


获取指定post的全部内容
https://bbs-api.mihoyo.com/post/wapi/getPostFull?gids=2&post_id=28894827&read=1