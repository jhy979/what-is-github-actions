# what is github actions
> ✨ 특정 이벤트에 따라 후속 작업을 할 수 있도록 github에서 지원해주는 기능입니다.

- 프로젝트를 진행하며 CI/CD를 도입했습니다. develop 브랜치에 merge될 때마다 테스트, 빌드, 린트 등 다양한 스크립트 명령어를 실행하며 코드의 품질과 유효성을 지속적으로 검증하면서 굉장히 편리하다고 느꼈습니다.

- 프로젝트의 적용점을 넘어서 조금 더 github actions를 유연하게 사용해보고자 학습하게 되었습니다.

- 🙌 예를 들면 figma token을 json 형태로 레포지터리에 가져올 수 있어요. 하지만 json 보다는 js나 css 파일 형태로 가져오면 좋을 것 같습니다. 그래서 `github actions`를 통해 json을 js나 css 파일 형태로 변경시켜주는 작업을 공부해보고자 합니다.

### 어디에 저장될까

> [레포지터리]/.github/workflows

---
### 이벤트 기반의 트리거
특정 이벤트가 발동할 경우 github actions가 동작합니다.

[많은 이벤트들이 있네요](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)

### `runs-on`
액션이 실행될 때 이 컴퓨터 환경에서 실행되면 좋겠어요.

---
### `steps`
실제 해야할 일들이예요.

#### name
실행될 액션의 이름이예요. (그냥 이름)

#### run
실행시킬 명령어예요.

#### uses
어떻게 제가 다 만듭니까~ 
다른 사람이 만든 액션들을 사용할게요. (마치 라이브러리 사용하듯이)

---
## github variable context
환경 변수를 활용할 수도 있어요.
[많은 variable context가 있습니다](https://docs.github.com/en/actions/learn-github-actions/contexts)


--
## secret info
settings -> secrets 들어가서 특정 정보를 은닉화할 수 있어요.

