# 목차
## [Formatter](#formatter)
---
Mac을 기준으로 합니다.

# Formatter
## prettier
### Prettier:Print Width
#### 코드를 과하게 수정할 때 다음과 같이 설정
`Fit code within this line limit`: 80 -> 160
### ~~python black formatter와 함께 쓰는 법~~
#### ~~cmd+shift+p > open workspace settings(json)~~
`.vscode/settings.json`
``` json
{
  "python.pythonPath": "",
  "editor.formatOnSave": true,
  "python.formatting.provider": "black",
  // "python.linting.pylintEnabled": true,
  // "python.linting.enabled": true,
  // "python.linting.lintOnSave": true,
  "[python]": {
    "editor.defaultFormatter": "ms-python.python"
  }
}
```
~~lint는 설치하지 않아서 주석처리~~
## black formatter
#### poetry에 설치
```
poetry add black
```
#### settings.json
- black을 설치한 poetry 가상환경에 `.vscode/settings.json`를 계속 새로 만드는 것이 불편  
- vscode 테마 수정할 때 `workbench.colorCustomizations`가 있는 settings.json 파일을 수정하면  
vscode 전체에 적용되므로 이 곳에 코드 작성
``` json
{ 
  // 아마 작성되어 있을 것임
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "prettier.printWidth": 110,
  /// 추가
  "python.formatting.provider": "black",
  "[python]": {
    "editor.defaultFormatter": "ms-python.python"
  }
}
```

#### prettierignore
`.prettierignore`
```
*.md
*.py
*.lock
*.toml
```

## 폰트크기
### 기본 
editor, terminal: 12