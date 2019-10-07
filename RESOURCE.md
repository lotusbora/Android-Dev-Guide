# Resource Guide

## Layout
- 레이아웃 형태에 따른 Prefix 정의(지속적 추가 예정)

| Prefix | 예시 | 설명 |
| ------------- | ------------- |------------- |
| `activity_` | activity_search | Activity용 Layout
| `fragment` | fragment_search | Fragment용 Layout
| `item` | item_room | RecyclerView Holder내의 Layout
| `view` | view_tag | CustomView 용 Layout
| `common` | common_appbar | include 또는 공통으로 사용될 Layout
| `dialog or CustomPopup` | dialog_market, popup_market | 다이얼로그 또는 팝업 용 레이아웃

## ID
- XML 내의 id Prefix 정의 (Kotlin 기반으로 정의)
- 하기 외의 레이아웃도 동일하게 CamelCase의 대문자 형태로 정의

| View | Prefix | example
| ------------- | ------------- |------------- |
| `TextView` | tv | tvTitle, tvDate 
| `ImageView` | tv | ivProfile 
| `RecyclerView` | rv | rvRoomList, rvComplexList 
| `EditText` | et | etName, etPassword
| `ProgressBar` | pb | pbLoading
| `CheckBox` | cb | cbAgree
| `Button` | bt | btStart, btConfirm 
| `ScrollView` | sv | svContainer
| `ConstrainLayout` | cl | clContainer
| `LinearLayout` | ll | llContainer

## String 
- `특정화면_설명` 형태로 작성(공통으로 사용될 경우 `common_설명`)

### 샘플
- search_title : 검색에서 사용되는 타이틀
- home_searchbar_hint : 홈에서 사용되는 검색바 힌트
- common_confirm : 버튼 공통으로 사용되는 확인 문구
- common_delete : 버튼 공통으로 사용되는 삭제 문구

## Drawable Selector
- Selected, Presssed, Focused, Disabled, Normal 등에 대한 Suffix
- 개발시에는 `_selector`

| 상태 | Suffix |
| ------------- | ------------- |
| Normal | `_normal` |
| Pressed | `_pressed` |
| Focused | `_focused` |
| Disabled | `_disabled` |
| Selected | `_selected` |

