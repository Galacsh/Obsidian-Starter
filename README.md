# 소개

## Obsidian

**Obsidian**은 여러 노트 앱 중 하나이다. 특이한 점이 있다면 다른 노트 앱과는 달리 마크다운 문법을 사용하기 때문에 개발자에게 가까운 앱이라는 것이다. 다만 표준 마크다운 문법에 추가적으로 Obsidian에서 지원하는 문법이 몇가지 있는데, 대표적으로 [Callout](https://help.obsidian.md/Editing+and+formatting/Callouts)이 있다.

## Vault

Obsidian을 처음 사용하게 되면 가장 먼저 만나게 될 단어는 아마 **Vault**일 것이다. Vault는 Obsidian에서 사용되는 용어로, 노트와 파일들이 저장되는 디렉토리(저장소)로 이해하면 편하다.

Obsidian에서 Vault로 어떤 디렉토리를 선택하게 되면, 그 디렉토리에는 `.obsidian` 이라는 숨김 폴더가 생성된다. 내부에는 Obsidian이 사용할 플러그인들이 설치되기도 하고, 플러그인이 관리하는 데이터나 Obsidian 설정 값들이 저장되게 된다.

이 말은 즉, `.obsidian` 파일과 디렉토리 구조를 미리 템플릿처럼 만들어두면 새로운 Obsidian Vault가 필요할 때마다 내 입맛대로 세팅이 되어있는 Vault를 생성해낼 수 있다는 뜻이다.

그래서 탄생한 것이 이 Vault Starter이다. 각종 플러그인, 테마 그리고 설정 값들까지 모두 내 입맛에 맞게 설정되어 있다.

> **참고**  
> [Obsidian 가이드](https://help.obsidian.md/Obsidian/Index)

## Starter 소개

이 Vault Starter에 대해서 간략히 정리하면 다음과 같다.

- Obsidian을 사용하면서 필수라고 생각하는 플러그인들 구성
- 맥OS 기준 단축키 구성
    - 원노트나 IDE를 사용하면서 손에 익은 단축키를 사용하려 노력하였음
- Git을 활용한 백업, 기기 간 동기화 지원
- 플러그인 수정
    - Excel to Markdown Table - 데스크탑 전용 플러그인으로 수정
        - IOS에서 지원되지 않는 Regex 관련 예외가 발생하여 처리함

---

# Starter 사용법

## 데스크탑

1. Github에서 동기화에 사용할 [Repository 생성](https://github.com/new)
    - e.g. **Repository Name:** Notes
    - Public or Private 무관
    - README, `.gitignore`, License 모두 추가하지 않음
2. [Obsidian-Starter-KR](https://github.com/Galacsh/Obsidian-Starter-KR) repository clone
3. Remote origin 변경 및 Push (하단 코드 참고)
4. Obsidian 실행
5. `Open folder as vault` 를 선택하여 Clone한 Repository 선택
6. Trust author and enable plugins
7. **Settings > Obsidian Git**
8. Commit Author 수정
    - `name`, `email`

```shell
git clone https://github.com/Galacsh/Obsidian-Starter-KR.git 'Notes'  
cd Notes  
git remote rename origin upstream  
git remote add origin https://github.com/USERNAME/Notes.git  
git push -u origin main  
```

## IOS

1. Obsidian 실행
2. `Create new vault`
	- "Store in iCloud" 설정 끄는 것 권장
3. **Settings > Community plugins**
    1. `Turn on community plugins`
    2. `Browse` 클릭
    3. **Obsidian Git** 검색
    4. 설치(`Install`) 및 허용(`Enable`)
4. `Options` 클릭
5. Commit Author 수정
    - Authentication/Commit Author
        - Github Username 입력
        - 비밀번호에 [PAT](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) 입력
            - Fine-grained personal access tokens
            - Fork 했던 Repository에 대해 발급
            - 권한
                - Contents : "Read and Write access"
                - Commit status : "Read and Write access"
                - Metadata : "Read access"
6. Settings 종료
7. "Command palette" 열고 `Obsidian Git: Clone existing remote repo`
8. Fork 된 Repository 경로 입력
	- 경로 끝에 반드시 `.git` 있는지 확인
9. "Vault Root" 선택
10. `.obsidian` 폴더를 다운로드 받도록 "YES" 선택
11. Obsidian 재시작
12. Settings > Obsidian Git
    - "Author name for commit" & "Author email for commit" 지정
