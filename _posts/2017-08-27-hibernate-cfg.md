---
layout: post
title: "hibernate配置文件"
description: ""
category: ""
tags: []
---
摘要：关于hibernate.cfg.xml配置文件的相关介绍

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE hibernate-configuration PUBLIC
    "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
    "http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">
<hibernate-configuration>
    <session-factory>
        <!-- 连接数据库的信息 -->
        <!-- mysql驱动信息 -->
        <property name="hibernate.connection.driver_class">com.mysql.jdbc.Driver</property>
        <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/Blog_DB</property>
        <!-- mysql数据库用户名 -->
        <property name="hibernate.connection.username">root</property>
        <!-- mysql数据库密码 -->
        <property name="hibernate.connection.password">19920902</property>

        <!-- 数据库的方言:根据底层的数据库生成不同的SQL -->
        <property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>
        <!-- 配置显示SQL -->
        <property name="hibernate.show_sql">true</property>
        <!-- 配置格式化SQL -->
        <property name="hibernate.format_sql">true</property>
		
		<!-- 连接池配置 -->
<!--         <property name="hibernate.connection.provider_class">org.hibernate.service.jdbc.connections.internal.C3P0ConnectionProvider</property>
 -->		
		<property name="connection.pool_size">1</property>
        <!--在连接池中可用的数据库连接的最少数目 -->
        <property name="c3p0.min_size">5</property>
        <!--在连接池中所有数据库连接的最大数目  -->
        <property name="c3p0.max_size">20</property>
        <!--设定数据库连接的过期时间,以秒为单位,
        如果连接池中的某个数据库连接处于空闲状态的时间超过了timeout时间,就会从连接池中清除 -->
        <property name="c3p0.timeout">120</property>
         <!--每3000秒检查所有连接池中的空闲连接 以秒为单位-->
        <property name="c3p0.idle_test_period">3000</property>

        <!-- 加载映射文件 -->
        <mapping resource="com/itschy/Model/User.hbm.xml"/>
    </session-factory>
</hibernate-configuration>
