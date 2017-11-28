## 后端API设计

* 一代API系统 /api/v1
    * 用户系统 /user
         * 账户系统 /auth
            * 登陆 /login
            * 注册 /signup
         * 个人账户 /detail/:id (:id为用户id)
            * TA关注的用户 /follows
            * TA的粉丝 /followers
            * TA发布的帖子 /post/
                * /:id (:id为帖子的id)(这个只会在前端出现)
    * 帖子系统 /post
        * 创建帖子 /create
        * 获取帖子 /detail/:id (:id为这个帖子的id)
            * 评论 /comment
                * 添加评论 /create
        * 投票 /vote
        * 点赞 /like
    * 搜索功能 /search
        * 关键字 ?{ keyword }
        