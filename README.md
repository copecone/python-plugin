# PythonMC (1.18+)

[![Kotlin](https://img.shields.io/badge/java-17-ED8B00.svg?logo=java&style=for-the-badge)](https://www.azul.com/)
[![Kotlin](https://img.shields.io/badge/kotlin-1.6.10-585DEF.svg?logo=kotlin&style=for-the-badge)](http://kotlinlang.org)
[![Gradle](https://img.shields.io/badge/gradle-7.3.3-02303A.svg?logo=gradle&style=for-the-badge)](https://gradle.org)
[![GitHub](https://img.shields.io/github/license/monun/paper-sample-lib-nms?style=for-the-badge)](https://www.gnu.org/licenses/gpl-3.0.html)
[![Kotlin](https://img.shields.io/badge/youtube-컨트롤D-red.svg?logo=youtube&style=for-the-badge)](https://www.youtube.com/channel/UCixrFCcSLF-E0AjNO9yNaqg)

## 프로젝트 구성하기

1. 저장소 복제 `git clone https://github.com/monun/paper-sample.git`
2. 프로젝트 이름 변경 (`settings.gradle.kts` 의 `rootProject.name`)
3. 구성 태스크 실행 `./gradlew setupModules`

---

```python
@command("hello", PlayerArgument("player"))
def hello(player -> PlayerInstance):
    # hello 명령어 썼을 때
    player.setName("Hello World!")

@event("onBreakBlock")
def onBreakBlock(event):
    # 블럭 부쉈을 때

event.enableEvent(onBreakBlock)
event.disableEvent(onBreakBlock)

# print("WASANS") -> [PRINT] WASANS -> 자바 -> WASANS 로그
# [EVENT] onBreakBlock, player ... -> 파이썬 -> 이벤트 함수 호출
```

---

#### API

최상위 계층 인터페이스

---

#### CORE

API의 구현, 실제 실행 코드

---

#### PLUGIN

PaperMC 와 상호작용할 JavaPlugin 을 포함한 코드

* `./gradlew pluginJar` Standalone 플러그인 빌드
* `./gradlew testJar` PUBLISH 프로젝트가 있을때 라이브러리를 참조하는 플러그인 빌드

---