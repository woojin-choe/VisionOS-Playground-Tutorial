# VisionOS-Playground-Tutorial
# Chapter 1 - Tunnel of Circles

## 📌 Summary (요약)
- SwiftUI와 visionOS의 기본 UI 요소를 활용해 원형 터널 형태의 인터랙티브 화면을 구현했다
- Slider와 ColorPicker를 이용해 깊이와 색상을 조절할 수 있도록 만들었다

## 🧠 What I Learned (배운 점)
- @State를 사용하면 값이 변경될 때 View가 자동으로 다시 그려진다
- ForEach를 사용해 반복적으로 View를 생성할 수 있다
- Grid와 GridRow를 활용하면 form 형태의 UI를 쉽게 정렬할 수 있다
- visionOS에서는 padding3D를 통해 요소를 3차원 방향으로 이동시킬 수 있다

## 🔍 Key Concepts (핵심 개념)
- @State: 상태값 저장 및 화면 갱신
- ForEach: 반복 View 생성
- Slider: 값 조절 UI
- ColorPicker: 색상 선택 UI
- Grid / GridRow: 표 형태 레이아웃 구성
- padding3D: visionOS의 3D 공간 이동
- background(.thickMaterial): 반투명 유리 느낌의 배경 효과

## 💡 What Was Interesting (흥미로웠던 점)
- Slider 값 하나만 변경해도 원들이 실시간으로 깊이감을 가지며 움직이는 부분이 인상적이었다
- ColorPicker를 통해 선택한 색상이 즉시 화면에 반영되는 구조가 흥미로웠다

## ❗ Difficulties (어려웠던 점)
- ColorPicker 내부 구조 때문에 label과 버튼 위치가 예상과 다르게 동작하는 부분이 처음에는 이해되지 않았다
- padding3D가 일반 padding과 어떤 차이가 있는지 처음에는 헷갈렸다

## ❓ Questions (궁금한 점)
- visionOS의 padding3D는 내부적으로 실제 3D 좌표를 어떻게 처리하는가?
- Grid와 HStack/VStack은 레이아웃 계산 방식이 어떻게 다른가?

## 🚀 Next Step (다음 단계)
- RealityKit과 연결해서 실제 3D 오브젝트를 배치해보기
- 사용자 제스처를 추가해 터널을 직접 회전하거나 확대해보기

# Chapter 2 - LabelMaker

## 📌 Summary (요약)
- TextField를 활용해 사용자가 직접 텍스트를 입력할 수 있는 UI를 구현했다
- 여러 줄 입력이 가능한 TextField를 만들고 스타일을 적용했다
- background, foregroundStyle, font 등을 사용해 입력창 디자인을 구성했다

## 🧠 What I Learned (배운 점)
- @State를 사용하면 TextField와 상태값을 실시간으로 연결할 수 있다
- Binding 문법인 `$변수명`을 통해 UI와 데이터를 양방향 연결할 수 있다
- axis: .vertical 옵션을 사용하면 여러 줄 입력이 가능해진다
- multilineTextAlignment를 사용해 여러 줄 텍스트 정렬을 설정할 수 있다

## 🔍 Key Concepts (핵심 개념)
- TextField: 사용자 입력 UI
- @State: 상태값 저장 및 View 자동 갱신
- Binding($): UI와 데이터 연결
- axis: .vertical: 세로 방향 입력 확장
- multilineTextAlignment: 여러 줄 텍스트 정렬
- background(_:in:): 특정 모양 안에 배경 적용
- RoundedRectangle: 둥근 모서리 사각형

## 💡 What Was Interesting (흥미로웠던 점)
- TextField가 단순 한 줄 입력창이 아니라 여러 줄 입력도 가능하다는 점이 흥미로웠다
- text 변수 값이 변경될 때마다 화면이 자동으로 갱신되는 SwiftUI 구조가 인상적이었다
- background 안에 RoundedRectangle을 직접 넣어서 UI 모양을 쉽게 변경할 수 있는 점이 재밌었다

## ❗ Difficulties (어려웠던 점)
- `$text`와 `text`의 차이를 처음에는 이해하기 어려웠다
- axis: .vertical이 TextEditor와 어떤 차이가 있는지 헷갈렸다
- multilineTextAlignment가 여러 줄 전체에 적용된다는 개념이 처음에는 익숙하지 않았다

## ❓ Questions (궁금한 점)
- TextField와 TextEditor는 내부적으로 어떤 차이가 있는가?
- SwiftUI의 Binding은 내부적으로 어떻게 상태를 연결하는가?
- visionOS에서는 TextField 입력 포커스를 어떤 방식으로 처리하는가?

## 🚀 Next Step (다음 단계)
- TextEditor를 활용해 메모장 형태의 UI 만들어보기
- 입력값 길이에 따라 UI가 동적으로 변하는 기능 추가해보기
- visionOS 스타일에 맞는 Glass UI 입력창 디자인 적용해보기

# Chapter 3 - Navigation

## 📌 Summary (요약)
- NavigationStack을 활용해 화면 이동 구조를 만들었다

## 🧠 What I Learned (배운 점)
- NavigationStack은 stack 기반으로 화면을 관리한다
- NavigationLink는 push 역할을 한다

## 🔍 Key Concepts (핵심 개념)
- NavigationStack: 화면 흐름 관리
- NavigationLink: 화면 이동 트리거

## 💡 What Was Interesting (흥미로웠던 점)
- 상태값만 바꿔도 화면 이동이 되는 구조가 인상적이었다

## ❗ Difficulties (어려웠던 점)
- NavigationDestination 구조가 처음에는 이해가 안됐다

## ❓ Questions (궁금한 점)
- NavigationStack과 UIKit의 UINavigationController는 내부적으로 어떻게 다른가?

## 🚀 Next Step (다음 단계)
- 실제 앱에서 여러 화면 흐름 만들어보기
