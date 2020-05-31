공주대학교 문서작성워크숍 2020 Spring에서 **BEAMER: 내용 중심의 프레젠테이션**을
주제로 발표한 자료입니다.

## 튜토리얼 자료 조판하기
[tutorial](./tutorial) 디렉터리 안에서 단계별 자료를 조판하시면 됩니다.
기본 pdfLaTeX으로도 조판이 가능합니다.

예컨대 `hello-beamer-9.tex` 자료를 조판하시려면
```sh
pdflatex hello-beamer-9.tex
```
으로 하시면 됩니다.
물론 `xelatex`이나 `lualatex`을 사용하셔도 문제 없습니다.

## 발표자료 조판하기
폰트는 Fira Sans, Noto Sans CJK KR, Noto Sans Mono와 Python 및 Pygments가
필요합니다.
폰트의 경우 없으시다면 macOS 기준 Homebrew로
```sh
brew tap homebrew/cask-fonts
brew cask install font-fira-sans font-fira-sans-mono font-noto-sans-cjk font-noto-sans-mono
```
설치하면 되고, Pygments의 경우 (설치하고자 하는 Python에서)
```sh
pip install Pygments
```
로 설치하시면 됩니다.
Windows나 Linux 등을 사용하시는 분들은 각 플랫폼에 알맞게 폰트랑 Pygments를
설치하시면 됩니다.

다른 폰트를 원하시는 경우LaTeX 파일의 `% Font Settings %` 부분을 수정하면
됩니다.

XeLaTeX으로 다음과 같이 (두어 번) 조판합니다:
```sh
xelatex --shell-escape beamer-tutorial.tex
```
