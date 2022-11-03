# 목차
## [Formatter](#formatter)
---
Mac을 기준으로 합니다.


# Formatter
## prettier
### Prettier:Print Width
#### 코드를 과하게 수정할 때 다음과 같이 설정
`Fit code within this line limit`: 80 -> 160
### python black formatter와 함께 쓰는 법
#### cmd+shift+p > open workspace settings(json)
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
lint는 설치하지 않아서 주석처리

#### prettierignore
`.prettierignore`
```
*.md
*.py
*.lock
*.toml
```