> [!tip]  
> Before reading more about this page, first read the [[Posts/Get Started/00. About|introduction]] about this repository.

# 📝 Memo

![Home](attachments/Home.png)

This page is powered by the [Homepage](https://obsidian.md/plugins?id=homepage) plugin. I installed it for these two main purposes.

- Instant Memos
- Daily tasks and completed tasks overview

I use the [Tasks](https://obsidian.md/plugins?id=obsidian-tasks-plugin) plugin to manage my daily tasks and completed tasks, and it can be used as follows:

~~~markdown
```tasks
not done
path does not include Templates/
sort by start
hide edit button
```
~~~

After writing the above code, tasks that need to be done are displayed as [[#🔥 To Do]]. Conversely, the following code displays completed tasks as [[#👍 Done]]:

~~~markdown
```tasks
done
path does not include _templates/
sort by done reverse
limit 20
hide edit button
```
~~~

Using Tasks specific query syntax, you can use `sort`, `group by`, and `limit` to see what you want. Refer to this [document](https://obsidian-tasks-group.github.io/) for more information.

---

# 🔥 To Do

```tasks
not done
path does not include Templates/
sort by start
hide edit button
```

# 👍 Done

```tasks
done
path does not include Templates/
sort by done reverse
limit 20
hide edit button

```
