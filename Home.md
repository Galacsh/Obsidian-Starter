> [!tip]  
> 이 페이지에 대한 내용을 더 읽어보기 전에, 우선 이 저장소에 대한 [[Posts/Get Started/00. About|소개]]를 읽어보자.

# 📝 메모

![Home](attachments/Home.png)

이 페이지는 [Homepage](https://obsidian.md/plugins?id=homepage) 플러그인을 이용해서 실행된다. 마지막에 작업 중이던 페이지에서 시작하거나 아무런 창도 없는 것도 좋지만, 개인적으로는 홈페이지가 있는 것을 선호하여 설치한 플러그인이다.

나는 [Homepage](https://obsidian.md/plugins?id=homepage) 플러그인을 크게 2가지 목적으로 사용한다.

- 즉석 메모
- 날짜별 할 일과 한 일 모아보기

날짜별 할 일과 한 일 모아보기는 [Tasks](https://obsidian.md/plugins?id=obsidian-tasks-plugin) 플러그인을 활용하여 처리하는데, 다음과 같이 사용할 수 있다.

~~~markdown
```tasks
not done
path does not include Templates/
sort by start
hide edit button
```
~~~

위 코드를 작성하고 나면 [[#🔥 To Do]] 와 같이 할 일이 표시된다. 반대로, 다음과 같이 작성하고 나면 [[#👍 Done]] 과 같이 한 일이 표시된다.

~~~markdown
```tasks
done
path does not include _templates/
sort by done reverse
limit 20
hide edit button
```
~~~

각각 유사 쿼리 문법을 이용하여 표현하는 방식으로 `sort`, `group by`, `limit` 을 이용하여 원하는 방식을 표현할 수 있으니 이 [문서](https://obsidian-tasks-group.github.io/) 를 참고하자.

---

# 🔥 To Do

```tasks
not done
path does not include 템플릿/
sort by start
hide edit button
```

# 👍 Done

```tasks
done
path does not include 템플릿/
sort by done reverse
limit 20
hide edit button

```
