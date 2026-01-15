# 📝 Flutter 할 일 관리 앱 (Todo List)

Flutter로 제작한 간단한 **할 일 관리(Todo List) 앱**입니다.  
사용자는 할 일을 추가하고, 완료 여부를 표시하거나 삭제할 수 있습니다.

---

## 📱 앱 개요

- 상태(State)를 사용하여 할 일 목록을 관리
- 한 화면에서 할 일 추가 / 완료 표시 / 삭제 가능

---

## ✨ 주요 기능

### 1. 할 일 추가
- 텍스트 입력창에 할 일을 입력
- `추가` 버튼 클릭 또는 키보드 Enter 시 목록에 추가됨

### 2. 할 일 완료 표시
- 할 일을 **누르면** 완료 상태로 변경
- 완료된 할 일은  
  - 취소선 표시  
  - 이탤릭체로 표시됨

### 3. 할 일 삭제
- 각 할 일 오른쪽의 **삭제 아이콘 버튼**을 누르면 해당 항목 삭제

---

## 🧱 코드 구조 설명

### `Todo` 클래스
```dart
class Todo {
  bool isDone;
  String title;
}
````

* 하나의 할 일을 표현하는 데이터 모델
* `title`: 할 일 내용
* `isDone`: 완료 여부

### `MyApp`

* 앱의 시작점
* `MaterialApp` 설정
* 첫 화면으로 `TodolistPage` 지정

### `TodolistPage` (StatefulWidget)

* 할 일 목록을 관리하는 메인 화면
* 내부 상태(State)로 할 일 리스트를 관리

#### 주요 상태 변수

* `List<Todo> _items` : 할 일 목록
* `TextEditingController _todoController` : 입력창 컨트롤러

#### 주요 메서드

* `_addTodo()` : 할 일 추가
* `_deleteTodo()` : 할 일 삭제
* `_toggleTodo()` : 완료 / 미완료 상태 전환

---

## 🛠 사용 기술

* Flutter
* Dart

---
