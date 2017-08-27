---
layout: post
title: "java代码高亮"
description: ""
category: ""
tags: []
---
java代码高亮的用法

java代码高亮的用法
{% highlight java linenos %}
public class UserDAO {
	public List<User> getUsers() {
		// 1.创建配置对象
		Configuration configuration = new Configuration().configure();
		ServiceRegistry serviceRegistry = new ServiceRegistryBuilder().applySettings(configuration.getProperties())
				.buildServiceRegistry();

		SessionFactory sessionFactory = configuration.buildSessionFactory(serviceRegistry);
		// 5.获取session对象
		Session session = sessionFactory.openSession();

		Query query = session.createQuery("from User");
		List<User> list = query.list();
		return list;
	}
}
{% endhighlight %}

更多关于Jekyll的信息，请访问：[Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
