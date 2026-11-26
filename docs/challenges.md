---
layout: page
title: "挑战注册表 · 已用题目"
permalink: /challenges/
---

# 挑战注册表 · 已用题目

本页由每篇链接页头部的 `challenges` 元数据自动汇总。
组装新一期之前先对一遍这张表：

| 日期 | 🟢 入门 | 🟡 进阶 | 🔴 挑战 |
| --- | --- | --- | --- |
{% for post in site.posts reversed %}{% assign e = post.challenges | where: "level", "easy" | first %}{% assign m = post.challenges | where: "level", "medium" | first %}{% assign h = post.challenges | where: "level", "hard" | first %}| {{ post.date | date: "%Y-%m-%d" }} | <a href="/{{ post.date | date: "%Y-%m-%d" }}/#easy">{{ e.title }}</a> | <a href="/{{ post.date | date: "%Y-%m-%d" }}/#medium">{{ m.title }}</a> | <a href="/{{ post.date | date: "%Y-%m-%d" }}/#hard">{{ h.title }}</a> |
{% endfor %}

机器可读版（JSON）：[/challenges.json](/challenges.json)，字段和帖子头部的元数据一致，供组装时自动查重。
