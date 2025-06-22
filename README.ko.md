<div align="center">
Fabric은 다음과 같은 분들의 아낌없는 지원을 받고 있습니다…

[![Github Repo Tagline](https://github.com/user-attachments/assets/96ab3d81-9b13-4df4-ba09-75dee7a5c3d2)](https://warp.dev/fabric)

<img src="./images/fabric-logo-gif.gif" alt="fabriclogo" width="400" height="400"/>

# `fabric`

![Static Badge](https://img.shields.io/badge/mission-human_flourishing_via_AI_augmentation-purple)
<br />
![GitHub top language](https://img.shields.io/github/languages/top/danielmiessler/fabric)
![GitHub last commit](https://img.shields.io/github/last-commit/danielmiessler/fabric)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

<div align="center">
<p class="align center">
<h4><code>fabric</code>은 AI를 사용하여 인간을 증강하는 오픈소스 프레임워크입니다.</h4>
</p>
</div>

[업데이트](#업데이트) •
[소개 및 필요성](#소개-및-필요성) •
[철학](#철학) •
[설치](#설치) •
[사용법](#사용법) •
[예시](#예시) •
[패턴 바로 사용하기](#패턴-바로-사용하기) •
[사용자 정의 패턴](#사용자-정의-패턴) •
[헬퍼 앱](#헬퍼-앱) •
[메타](#메타)

![Screenshot of fabric](images/fabric-summarize.png)

</div>

## 소개 및 필요성

2022년 말 현대 AI가 시작된 이래로 작업을 수행하기 위한 **_엄청난_** 수의 AI 애플리케이션을 보아왔습니다. 세상의 모든 다양한 AI를 사용하기 위한 수천 개의 웹사이트, 챗봇, 모바일 앱 및 기타 인터페이스가 있습니다.

모든 것이 정말 흥미롭고 강력하지만, _이 기능을 우리 삶에 통합하는 것은 쉽지 않습니다._

<p class="align center">
<h4>즉, AI는 능력의 문제가 아니라 <em>통합</em>의 문제입니다.</h4>
</p>

**Fabric은 AI의 기본 단위인 프롬프트 자체를 만들고 구성하여 이 문제를 해결하기 위해 만들어졌습니다!**

Fabric은 실제 작업을 기준으로 프롬프트를 구성하여 사람들이 가장 중요한 AI 솔루션을 즐겨 사용하는 도구에서 사용할 수 있도록 단일 장소에서 만들고, 수집하고, 구성할 수 있도록 합니다. 그리고 명령줄에 익숙하다면 Fabric 자체를 인터페이스로 사용할 수 있습니다!

## 소개 영상

이러한 영상 중 다수는 Fabric이 Python 기반일 때 녹화되었으므로 아래의 현재 [설치 지침](#설치)을 사용해야 합니다.

- [Network Chuck](https://www.youtube.com/watch?v=UbDyjIIGaxQ)
- [David Bombal](https://www.youtube.com/watch?v=vF-MQmVxnCs)
- [My Own Intro to the Tool](https://www.youtube.com/watch?v=wPEyyigh10g)
- [More Fabric YouTube Videos](https://www.youtube.com/results?search_query=fabric+ai)


## 탐색

- [`fabric`](#fabric)
  - [탐색](#탐색)
  - [업데이트](#업데이트)
  - [소개 및 필요성](#소개-및-필요성)
  - [소개 영상](#소개-영상)
  - [철학](#철학)
    - [문제를 구성 요소로 분해](#문제를-구성-요소로-분해)
    - [너무 많은 프롬프트](#너무-많은-프롬프트)
  - [설치](#설치)
    - [최신 릴리스 바이너리 가져오기](#최신-릴리스-바이너리-가져오기)
      - [Windows](#windows)
      - [macOS (arm64)](#macos-arm64)
      - [macOS (amd64)](#macos-amd64)
      - [Linux (amd64)](#linux-amd64)
      - [Linux (arm64)](#linux-arm64)
    - [패키지 관리자 사용](#패키지-관리자-사용)
      - [macOS (Homebrew)](#macos-homebrew)
      - [Arch Linux (AUR)](#arch-linux-aur)
    - [소스에서 설치](#소스에서-설치)
    - [환경 변수](#환경-변수)
    - [설정](#설정)
    - [모든 패턴에 대한 별칭 추가](#모든-패턴에-대한-별칭-추가)
      - [별칭을 사용하여 마크다운으로 파일 저장](#별칭을-사용하여-마크다운으로-파일-저장)
    - [마이그레이션](#마이그레이션)
    - [업그레이드](#업그레이드)
    - [셸 자동 완성](#셸-자동-완성)
      - [Zsh 자동 완성](#zsh-자동-완성)
      - [Bash 자동 완성](#bash-자동-완성)
      - [Fish 자동 완성](#fish-자동-완성)
  - [사용법](#사용법)
  - [프롬프트 접근 방식](#프롬프트-접근-방식)
  - [예시](#예시)
  - [패턴 바로 사용하기](#패턴-바로-사용하기)
    - [프롬프트 전략](#프롬프트-전략)
  - [사용자 정의 패턴](#사용자-정의-패턴)
  - [헬퍼 앱](#헬퍼-앱)
    - [`to_pdf`](#to_pdf)
    - [`to_pdf` 설치](#to_pdf-설치)
    - [`code_helper`](#code_helper)
  - [pbpaste](#pbpaste)
  - [웹 인터페이스](#웹-인터페이스)
    - [설치](#설치-1)
    - [Streamlit UI](#streamlit-ui)
      - [클립보드 지원](#클립보드-지원)
  - [메타](#메타)
    - [주요 기여자](#주요-기여자)
    - [기여자](#기여자)

<br />

## 업데이트

> [!NOTE]
>
>2025년 6월 17일
>
>- 이제 Fabric은 Perplexity AI를 지원합니다. `fabric -S`를 사용하여 Perlexity AI API 키를 추가하여 구성한 다음 다음을 시도하십시오.
>
>   ```bash
>   fabric -m sonar-pro "What is the latest world news?"
>   ```
>
>2025년 6월 11일
>
>- 이제 Fabric의 YouTube 스크립트 변환에는 `yt-dlp`가 설치되어 있어야 합니다. 최신 버전을 설치하십시오.
> (이 노트 작성 시점 기준 2025.06.09). YouTube API 키는 댓글(`--comments` 플래그) 및
> 메타데이터 추출(`--metadata` 플래그)에만 필요합니다.

## 철학

> AI는 그 자체가 아니라 어떤 것을 _확대하는 도구_입니다. 그리고 그 어떤 것은 바로 **인간의 창의성**입니다.

우리는 기술의 목적이 인간의 번영을 돕는 것이라고 믿으므로, AI에 대해 이야기할 때는 우리가 해결하고자 하는 **인간**의 문제에서 시작합니다.

### 문제를 구성 요소로 분해

우리의 접근 방식은 문제를 개별적인 부분으로 나누고(아래 참조) 그런 다음 한 번에 하나씩 AI를 적용하는 것입니다. 몇 가지 예는 아래를 참조하십시오.

<img width="2078" alt="augmented_challenges" src="https://github.com/danielmiessler/fabric/assets/50654/31997394-85a9-40c2-879b-b347e4701f06">

### 너무 많은 프롬프트

프롬프트는 이에 적합하지만, 2023년에 제가 직면했던 가장 큰 과제(오늘날에도 여전히 존재함)는 **세상에 너무 많은 AI 프롬프트가 있다는 것**입니다. 우리 모두에게 유용한 프롬프트가 있지만, 새로운 프롬프트를 발견하고, 좋은지 아닌지 알고, _우리가 좋아하는 프롬프트의 다른 버전을 관리하는 것_은 어렵습니다.

`fabric`의 주요 기능 중 하나는 사람들이 _패턴_이라고 부르는 프롬프트를 수집하고 삶의 다양한 부분에 통합하도록 돕는 것입니다.

Fabric에는 다음과 같은 다양한 생활 및 업무 활동을 위한 패턴이 있습니다.

- YouTube 동영상 및 팟캐스트에서 가장 흥미로운 부분 추출
- 아이디어만으로 자신의 목소리로 에세이 작성
- 난해한 학술 논문 요약
- 글에 완벽하게 어울리는 AI 아트 프롬프트 생성
- 전체 내용을 읽거나 볼 가치가 있는지 콘텐츠 품질 평가
- 길고 지루한 콘텐츠 요약 받기
- 코드 설명 듣기
- 사용하기 어려운 문서를 유용한 문서로 변환
- 모든 콘텐츠 입력에서 소셜 미디어 게시물 생성
- 그리고 백만 가지 이상의 다른 기능…

## 설치

Fabric을 설치하려면 최신 릴리스 바이너리를 사용하거나 소스에서 설치할 수 있습니다.

### 최신 릴리스 바이너리 가져오기

#### Windows

`https://github.com/danielmiessler/fabric/releases/latest/download/fabric-windows-amd64.exe`

#### macOS (arm64)

`curl -L https://github.com/danielmiessler/fabric/releases/latest/download/fabric-darwin-arm64 > fabric && chmod +x fabric && ./fabric --version`

#### macOS (amd64)

`curl -L https://github.com/danielmiessler/fabric/releases/latest/download/fabric-darwin-amd64 > fabric && chmod +x fabric && ./fabric --version`

#### Linux (amd64)

`curl -L https://github.com/danielmiessler/fabric/releases/latest/download/fabric-linux-amd64 > fabric && chmod +x fabric && ./fabric --version`

#### Linux (arm64)

`curl -L https://github.com/danielmiessler/fabric/releases/latest/download/fabric-linux-arm64 > fabric && chmod +x fabric && ./fabric --version`

### 패키지 관리자 사용

**참고:** Homebrew 또는 Arch Linux 패키지 관리자를 사용하면 `fabric`이 `fabric-ai`로 제공되므로, 이를 고려하여 셸 시작 파일에 다음 별칭을 추가하십시오.

```bash
alias fabric='fabric-ai'
```

#### macOS (Homebrew)

`brew install fabric-ai`

#### Arch Linux (AUR)

`yay -S fabric-ai`

### 소스에서 설치

Fabric을 설치하려면 [Go가 설치되어 있는지 확인](https://go.dev/doc/install)한 다음 다음 명령을 실행하십시오.

```bash
# 저장소에서 직접 Fabric 설치
go install github.com/danielmiessler/fabric@latest
```

### 환경 변수

`fabric` 명령을 실행하려면 Linux의 `~/.bashrc` 또는 Mac의 `~/.zshrc` 파일에 일부 환경 변수를 설정해야 할 수 있습니다. 추가할 수 있는 항목의 예는 다음과 같습니다.

Intel 기반 Mac 또는 Linux의 경우

```bash
# Golang 환경 변수
export GOROOT=/usr/local/go
export GOPATH=$HOME/go

# GOPATH 및 GOROOT 바이너리를 포함하도록 PATH 업데이트
export PATH=$GOPATH/bin:$GOROOT/bin:$HOME/.local/bin:$PATH
```

Apple Silicon 기반 Mac의 경우

```bash
# Golang 환경 변수
export GOROOT=$(brew --prefix go)/libexec
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$HOME/.local/bin:$PATH
```

### 설정

이제 다음 명령을 실행하십시오.

```bash
# 디렉터리와 키를 설정하기 위해 설정 실행
fabric --setup
```

모든 것이 작동하면 준비가 된 것입니다.

### 모든 패턴에 대한 별칭 추가

모든 패턴에 대한 별칭을 추가하고 `summarize` 대신 `fabric --pattern summarize`와 같이 명령으로 직접 사용하려면 `.zshrc` 또는 `.bashrc` 파일에 다음을 추가할 수 있습니다.

```bash
# ~/.config/fabric/patterns 디렉터리의 모든 파일을 반복합니다.
for pattern_file in $HOME/.config/fabric/patterns/*; do
    # 파일의 기본 이름 가져오기(즉, 디렉터리 경로 제거)
    pattern_name=$(basename "$pattern_file")

    # alias pattern_name="fabric --pattern pattern_name" 형식으로 별칭 만들기
    alias_command="alias $pattern_name='fabric --pattern $pattern_name'"

    # 현재 셸에 추가하기 위해 별칭 명령 평가
    eval "$alias_command"
done

yt() {
    if [ "$#" -eq 0 ] || [ "$#" -gt 2 ]; then
        echo "사용법: yt [-t | --timestamps] youtube-link"
        echo "타임스탬프가 있는 스크립트를 얻으려면 '-t' 플래그를 사용하십시오."
        return 1
    fi

    transcript_flag="--transcript"
    if [ "$1" = "-t" ] || [ "$1" = "--timestamps" ]; then
        transcript_flag="--transcript-with-timestamps"
        shift
    fi
    local video_link="$1"
    fabric -y "$video_link" $transcript_flag
}
```

PowerShell 창에서 `notepad $PROFILE`을 실행하여 PowerShell 내부에 해당하는 별칭에 대해 아래 코드를 추가할 수 있습니다.

```powershell
# 패턴 디렉터리 경로
$patternsPath = Join-Path $HOME ".config/fabric/patterns"
foreach ($patternDir in Get-ChildItem -Path $patternsPath -Directory) {
    $patternName = $patternDir.Name

    # 각 패턴에 대해 동적으로 함수 정의
    $functionDefinition = @"
function $patternName {
    [CmdletBinding()]
    param(
        [Parameter(ValueFromPipeline = `$true)]
        [string] `$InputObject,

        [Parameter(ValueFromRemainingArguments = `$true)]
        [String[]] `$patternArgs
    )

    begin {
        # 파이프라인 입력을 수집하기 위한 배열 초기화
        `$collector = @()
    }

    process {
        # 파이프라인 입력 개체 수집
        if (`$InputObject) {
            `$collector += `$InputObject
        }
    }

    end {
        # 모든 파이프라인 입력을 줄 바꿈으로 구분된 단일 문자열로 결합
        `$pipelineContent = `$collector -join "`n"

        # 파이프라인 입력이 있는 경우 fabric 호출에 포함
        if (`$pipelineContent) {
            `$pipelineContent | fabric --pattern $patternName `$patternArgs
        } else {
            # 파이프라인 입력 없음; 추가 인수로 fabric 호출
            fabric --pattern $patternName `$patternArgs
        }
    }
}
"@
    # 현재 세션에 함수 추가
    Invoke-Expression $functionDefinition
}

# 'yt' 함수도 정의
function yt {
    [CmdletBinding()]
    param(
        [Parameter()]
        [Alias("timestamps")]
        [switch]$t,

        [Parameter(Position = 0, ValueFromPipeline = $true)]
        [string]$videoLink
    )

    begin {
        $transcriptFlag = "--transcript"
        if ($t) {
            $transcriptFlag = "--transcript-with-timestamps"
        }
    }

    process {
        if (-not $videoLink) {
            Write-Error "사용법: yt [-t | --timestamps] youtube-link"
            return
        }
    }

    end {
        if ($videoLink) {
            # 실행하고 출력이 파이프라인을 통해 흐르도록 허용
            fabric -y $videoLink $transcriptFlag
        }
    }
}
```

이렇게 하면 `yt https://www.youtube.com/watch?v=4b0iet22VIk`를 사용하여 스크립트, 댓글 및 메타데이터를 가져올 수 있는 `yt` 별칭도 만들어집니다.

#### 별칭을 사용하여 마크다운으로 파일 저장

위의 별칭 외에도 출력을 Obsidian과 같은 즐겨 사용하는 마크다운 노트 저장소에 저장하는 옵션을 사용하려면 위의 내용 대신 `.zshrc` 또는 `.bashrc` 파일에 다음을 추가하십시오.

```bash
# Obsidian 노트의 기본 디렉터리 정의
obsidian_base="/path/to/obsidian"

# ~/.config/fabric/patterns 디렉터리의 모든 파일을 반복합니다.
for pattern_file in ~/.config/fabric/patterns/*; do
    # 파일의 기본 이름 가져오기(즉, 디렉터리 경로 제거)
    pattern_name=$(basename "$pattern_file")

    # 동일한 이름의 기존 별칭 제거
    unalias "$pattern_name" 2>/dev/null

    # 각 패턴에 대해 동적으로 함수 정의
    eval "
    $pattern_name() {
        local title=\$1
        local date_stamp=\$(date +'%Y-%m-%d')
        local output_path=\"\$obsidian_base/\${date_stamp}-\${title}.md\"

        # 제목이 제공되었는지 확인
        if [ -n \"\$title\" ]; then
            # 제목이 제공되면 출력 경로 사용
            fabric --pattern \"$pattern_name\" -o \"\$output_path\"
        else
            # 제목이 제공되지 않으면 --stream 사용
            fabric --pattern \"$pattern_name\" --stream
        fi
    }
    "
done
```

이렇게 하면 위에서처럼 `summarize` 대신 `fabric --pattern summarize --stream`과 같이 패턴을 별칭으로 사용할 수 있지만, `summarize "my_article_title"`과 같이 추가 인수를 전달하면 `obsidian_base="/path/to/obsidian"`에 설정한 대상에 `YYYY-MM-DD-my_article_title.md` 형식으로 출력이 저장되며 날짜는 자동으로 생성됩니다.
`date_stamp` 형식을 조정하여 날짜 형식을 조정할 수 있습니다.

### 마이그레이션

레거시(Python) 버전이 설치되어 있고 Go 버전으로 마이그레이션하려면 다음과 같이 하십시오. 기본적으로 두 단계입니다. 1) Python 버전 제거, 2) Go 버전 설치.

```bash
# 레거시 Fabric 제거
pipx uninstall fabric

# 이전 Fabric 별칭 지우기
(.bashrc, .zshrc 등 확인)
# Go 버전 설치
go install github.com/danielmiessler/fabric@latest
# 새 버전에 대한 설정 실행. 변경 사항이 있으므로 중요합니다.
fabric --setup
```

그런 다음 위와 같이 [환경 변수를 설정](#환경-변수)하십시오.

### 업그레이드

Go의 가장 큰 장점은 업그레이드가 매우 쉽다는 것입니다. 처음에 설치하는 데 사용한 것과 동일한 명령을 실행하면 항상 최신 버전을 얻을 수 있습니다.

```bash
go install github.com/danielmiessler/fabric@latest
```

### 셸 자동 완성

Fabric은 Zsh, Bash 및 Fish 셸에 대한 셸 자동 완성 스크립트를 제공하여 명령 및 옵션에 대한 탭 완성을 제공함으로써 CLI를 더 쉽게 사용할 수 있도록 합니다.

#### Zsh 자동 완성

Zsh 자동 완성을 활성화하려면:

```bash
# 자동 완성 파일을 $fpath의 디렉터리로 복사
mkdir -p ~/.zsh/completions
cp completions/_fabric ~/.zsh/completions/

# compinit 전에 .zshrc의 fpath에 디렉터리 추가
echo 'fpath=(~/.zsh/completions $fpath)' >> ~/.zshrc
echo 'autoload -Uz compinit && compinit' >> ~/.zshrc
```

#### Bash 자동 완성

Bash 자동 완성을 활성화하려면:

```bash
# .bashrc에서 자동 완성 스크립트 소싱
echo 'source /path/to/fabric/completions/fabric.bash' >> ~/.bashrc

# 또는 시스템 전체 bash 자동 완성 디렉터리로 복사
sudo cp completions/fabric.bash /etc/bash_completion.d/
```

#### Fish 자동 완성

Fish 자동 완성을 활성화하려면:

```bash
# 자동 완성 파일을 fish 자동 완성 디렉터리로 복사
mkdir -p ~/.config/fish/completions
cp completions/fabric.fish ~/.config/fish/completions/
```

## 사용법

모두 설정했으면 다음과 같이 사용하십시오.

```bash
fabric -h
```

```plaintext

사용법:
  fabric [옵션]

애플리케이션 옵션:
  -p, --pattern=                    사용 가능한 패턴 중에서 패턴 선택
  -v, --variable=                   패턴 변수 값, 예: -v=#role:expert -v=#points:30
  -C, --context=                    사용 가능한 컨텍스트 중에서 컨텍스트 선택
      --session=                    사용 가능한 세션 중에서 세션 선택
  -a, --attachment=                 첨부 파일 경로 또는 URL (예: OpenAI 이미지 인식 메시지용)
  -S, --setup                       fabric의 모든 재구성 가능한 부분에 대한 설정 실행
  -t, --temperature=                온도 설정 (기본값: 0.7)
  -T, --topp=                       상위 P 설정 (기본값: 0.9)
  -s, --stream                      스트림
  -P, --presencepenalty=            존재 패널티 설정 (기본값: 0.0)
  -r, --raw                         채팅 옵션(온도 등)을 보내지 않고 모델의 기본값을 사용하고 패턴에 대해 시스템 역할 대신 사용자 역할을 사용합니다.
  -F, --frequencypenalty=           빈도 패널티 설정 (기본값: 0.0)
  -l, --listpatterns                모든 패턴 나열
  -L, --listmodels                  사용 가능한 모든 모델 나열
  -x, --listcontexts                모든 컨텍스트 나열
  -X, --listsessions                모든 세션 나열
  -U, --updatepatterns              패턴 업데이트
  -c, --copy                        클립보드에 복사
  -m, --model=                      모델 선택
      --modelContextLength=         모델 컨텍스트 길이 (ollama에만 영향)
  -o, --output=                     파일로 출력
      --output-session              전체 세션(임시 세션 포함)을 출력 파일로 출력
  -n, --latest=                     나열할 최신 패턴 수 (기본값: 0)
  -d, --changeDefaultModel          기본 모델 변경
  -y, --youtube=                    YouTube 동영상 또는 재생 목록 "URL"에서 스크립트, 댓글을 가져와 채팅으로 보내거나 콘솔에 인쇄하고 출력 파일에 저장
      --playlist                    URL에 두 ID가 모두 있는 경우 동영상보다 재생 목록 우선
      --transcript                  YouTube 동영상에서 스크립트를 가져와 채팅으로 보냅니다(기본적으로 사용됨).
      --transcript-with-timestamps  타임스탬프가 있는 YouTube 동영상에서 스크립트를 가져와 채팅으로 보냅니다.
      --comments                    YouTube 동영상에서 댓글을 가져와 채팅으로 보냅니다.
      --metadata                    동영상 메타데이터 출력
  -g, --language=                   채팅 언어 코드 지정, 예: -g=en -g=zh
  -u, --scrape_url=                 Jina AI를 사용하여 웹사이트 URL을 마크다운으로 스크랩
  -q, --scrape_question=            Jina AI를 사용하여 질문 검색
  -e, --seed=                       LMM 생성에 사용할 시드
  -w, --wipecontext=                컨텍스트 지우기
  -W, --wipesession=                세션 지우기
      --printcontext=               컨텍스트 인쇄
      --printsession=               세션 인쇄
      --readability                 HTML 입력을 깨끗하고 읽기 쉬운 보기로 변환
      --input-has-vars              사용자 입력에 변수 적용
      --dry-run                     실제로 보내지 않고 모델로 보낼 내용 표시
      --serve                       Fabric Rest API 제공
      --serveOllama                 ollama 엔드포인트로 Fabric Rest API 제공
      --address=                    REST API를 바인딩할 주소 (기본값: :8080)
      --api-key=                    서버 경로를 보호하는 데 사용되는 API 키
      --config=                     YAML 구성 파일 경로
      --version                     현재 버전 인쇄
      --listextensions              등록된 모든 확장 프로그램 나열
      --addextension=               구성 파일 경로에서 새 확장 프로그램 등록
      --rmextension=                이름으로 등록된 확장 프로그램 제거
      --strategy=                   사용 가능한 전략 중에서 전략 선택
      --liststrategies              모든 전략 나열
      --listvendors                 모든 공급업체 나열
      --shell-complete-list         헤더/서식 없이 원시 목록 출력 (셸 자동 완성용)

도움말 옵션:
  -h, --help                        이 도움말 메시지 표시

```

## 프롬프트 접근 방식

Fabric _패턴_은 대부분의 프롬프트와 다릅니다.

- **첫째, 가독성과 편집성을 최대한 보장하기 위해 `Markdown`을 사용합니다.** 이는 제작자가 좋은 패턴을 만드는 데 도움이 될 뿐만 아니라 패턴의 작동 방식을 깊이 이해하려는 모든 사람에게도 도움이 됩니다. _중요하게도, 이는 패턴을 보내는 AI에도 해당됩니다!_

다음은 Fabric 패턴의 예입니다.

```bash
https://github.com/danielmiessler/fabric/blob/main/patterns/extract_wisdom/system.md
```

<img width="1461" alt="pattern-example" src="https://github.com/danielmiessler/fabric/assets/50654/b910c551-9263-405f-9735-71ca69bbab6d">

- **다음으로, 지침이 매우 명확하며** Markdown 구조를 사용하여 AI가 수행하기를 원하는 작업과 순서를 강조합니다.

- **마지막으로, 프롬프트의 시스템 섹션을 거의 독점적으로 사용하는 경향이 있습니다.** 1년 넘게 이 작업에 몰두한 결과, 그렇게 하는 것이 더 효과적이라는 것을 알게 되었습니다. 상황이 바뀌거나 그렇지 않다는 데이터가 나오면 조정할 것입니다.

## 예시

> 다음 예시에서는 macOS `pbpaste`를 사용하여 클립보드에서 붙여넣습니다. Windows 및 Linux 대안은 아래 [pbpaste](#pbpaste) 섹션을 참조하십시오.

이제 Fabric으로 할 수 있는 몇 가지 작업을 살펴보겠습니다.

1. `stdin`의 입력을 기반으로 `summarize` 패턴을 실행합니다. 이 경우 기사의 본문입니다.

    ```bash
    pbpaste | fabric --pattern summarize
    ```

2. `--stream` 옵션과 함께 `analyze_claims` 패턴을 실행하여 즉각적이고 스트리밍되는 결과를 얻습니다.

    ```bash
    pbpaste | fabric --stream --pattern analyze_claims
    ```

3. `--stream` 옵션과 함께 `extract_wisdom` 패턴을 실행하여 모든 YouTube 동영상에서 즉각적이고 스트리밍되는 결과를 얻습니다(원래 소개 동영상과 매우 유사).

    ```bash
    fabric -y "https://youtube.com/watch?v=uXs-zPc63kM" --stream --pattern extract_wisdom
    ```

4. 패턴 만들기 - 패턴이 포함된 .md 파일을 만들어 `~/.config/fabric/patterns/[yourpatternname]`에 저장해야 합니다.

5. 웹사이트에서 `analyze_claims` 패턴을 실행합니다. Fabric은 Jina AI를 사용하여 URL을 마크다운 형식으로 스크랩한 후 모델로 보냅니다.

    ```bash
    fabric -u https://github.com/danielmiessler/fabric/ -p analyze_claims
    ```

## 패턴 바로 사용하기

<img width="1173" alt="fabric-patterns-screenshot" src="https://github.com/danielmiessler/fabric/assets/50654/9186a044-652b-4673-89f7-71cf066f32d8">

<br />
<br />

특별한 작업을 하려는 것이 아니라 훌륭한 프롬프트를 많이 원한다면 [`/patterns`](https://github.com/danielmiessler/fabric/tree/main/patterns) 디렉터리로 이동하여 탐색을 시작할 수 있습니다!

Fabric에서 다른 것을 사용하지 않더라도 패턴 자체만으로도 프로젝트가 유용해지기를 바랍니다.

ChatGPT든 다른 앱이나 웹사이트든 관계없이 가지고 있는 모든 AI 애플리케이션에서 볼 수 있는 모든 패턴을 사용할 수 있습니다. 우리의 계획과 예측은 사람들이 곧 우리가 게시한 것보다 훨씬 더 많은 패턴을 공유할 것이며, 우리 것보다 훨씬 더 나을 것이라는 것입니다.

집단 지성의 승리입니다.

### 프롬프트 전략

Fabric은 또한 "사고의 연쇄" 또는 "초안의 연쇄"와 같은 프롬프트 전략을 구현하며, 이는 기본 패턴 외에도 사용할 수 있습니다.

프롬프트 전략의 예는 [더 적게 쓰고 더 빠르게 생각하기](https://arxiv.org/pdf/2502.18600) 논문과 [프롬프트 학습의 사고 생성 섹션](https://learnprompting.org/docs/advanced/thought_generation/introduction)을 참조하십시오.

각 전략은 [`/strategies`](https://github.com/danielmiessler/fabric/tree/main/strategies) 디렉터리의 작은 `json` 파일로 제공됩니다.

전략의 프롬프트 수정은 시스템 프롬프트에 적용되어 채팅 세션의 LLM으로 전달됩니다.

`fabric -S`를 사용하고 `~/.config/fabric` 디렉터리에 전략을 설치하는 옵션을 선택하십시오.

## 사용자 정의 패턴

Fabric을 사용하여 자신만의 사용자 정의 패턴을 만들고 싶지만 다른 사람과 공유하고 싶지 않을 수 있습니다. 문제 없습니다!

`~/.config/custompatterns/` (또는 원하는 위치)에 디렉터리를 만들고 `.md` 파일을 거기에 넣으십시오.

사용할 준비가 되면 `~/.config/fabric/patterns/`로 복사하십시오.

그런 다음 다른 패턴처럼 사용할 수 있지만 Fabric 프로젝트에 풀 리퀘스트로 명시적으로 제출하지 않는 한 공개되지 않습니다. 그러니 걱정하지 마십시오. 비공개입니다.

## 헬퍼 앱

Fabric은 또한 다양한 워크플로와 더 쉽게 통합할 수 있도록 몇 가지 핵심 헬퍼 앱(도구)을 사용합니다. 다음은 몇 가지 예입니다.

### `to_pdf`

`to_pdf`는 LaTeX 파일을 PDF 형식으로 변환하는 헬퍼 명령입니다. 다음과 같이 사용할 수 있습니다.

```bash
to_pdf input.tex
```

이렇게 하면 동일한 디렉터리에 입력 LaTeX 파일에서 PDF 파일이 만들어집니다.

`write_latex` 패턴과 완벽하게 작동하는 stdin과 함께 사용할 수도 있습니다.

```bash
echo "ai security primer" | fabric --pattern write_latex | to_pdf
```

이렇게 하면 현재 디렉터리에 `output.pdf`라는 PDF 파일이 만들어집니다.

### `to_pdf` 설치

`to_pdf`를 설치하려면 Fabric을 설치하는 것과 동일한 방식으로 다른 저장소 이름으로 설치하십시오.

```bash
go install github.com/danielmiessler/fabric/plugins/tools/to_pdf@latest
```

시스템에 LaTeX 배포판(예: TeX Live 또는 MiKTeX)이 설치되어 있는지 확인하십시오. `to_pdf`는 시스템의 PATH에서 `pdflatex`를 사용할 수 있어야 합니다.

### `code_helper`

`code_helper`는 `create_coding_feature` 패턴과 함께 사용됩니다.
새로운 기능을 만들거나 지정된 방식으로 코드를 편집하라는 지침과 함께 AI 모델에 제공할 수 있는 코드 디렉터리의 `json` 표현을 생성합니다.

자세한 내용은 [코딩 기능 패턴 만들기 README](./patterns/create_coding_feature/README.md)를 참조하십시오.

먼저 다음을 사용하여 설치하십시오.

```bash
go install github.com/danielmiessler/fabric/plugins/tools/code_helper@latest
```

## pbpaste

[예시](#예시)에서는 macOS 프로그램 `pbpaste`를 사용하여 클립보드의 내용을 `fabric`에 입력으로 파이프합니다. `pbpaste`는 Windows 또는 Linux에서 사용할 수 없지만 대안이 있습니다.

Windows에서는 PowerShell 명령 프롬프트에서 PowerShell 명령 `Get-Clipboard`를 사용할 수 있습니다. 원하는 경우 `pbpaste`에 대한 별칭을 만들 수도 있습니다. 클래식 PowerShell을 사용하는 경우 `~\Documents\WindowsPowerShell\.profile.ps1` 파일을 편집하거나 PowerShell Core를 사용하는 경우 `~\Documents\PowerShell\.profile.ps1`을 편집하고 별칭을 추가하십시오.

```powershell
Set-Alias pbpaste Get-Clipboard
```

Linux에서는 `xclip -selection clipboard -o`를 사용하여 클립보드에서 붙여넣을 수 있습니다. 패키지 관리자를 사용하여 `xclip`을 설치해야 할 가능성이 높습니다. Ubuntu를 포함한 Debian 기반 시스템의 경우,

```sh
sudo apt update
sudo apt install xclip -y
```

`~/.bashrc` 또는 `~/.zshrc`를 편집하고 별칭을 추가하여 별칭을 만들 수도 있습니다.

```sh
alias pbpaste='xclip -selection clipboard -o'
```

## 웹 인터페이스

이제 Fabric에는 명령줄 인터페이스에 대한 GUI 대안과 웹 개발 또는 블로깅을 시작하려는 사람들을 위한 즉시 사용 가능한 웹사이트를 제공하는 내장 웹 인터페이스가 포함되어 있습니다.
이 앱을 Fabric용 GUI 인터페이스, 바로 사용할 수 있는 블로그 사이트 또는 자신만의 프로젝트를 위한 웹사이트 템플릿으로 사용할 수 있습니다.

`web/src/lib/content` 디렉터리에는 시작 `.obsidian/` 및 `templates/` 디렉터리가 포함되어 있어 `web/src/lib/content/` 디렉터리를 [Obsidian.md](https://obsidian.md) 저장소로 열 수 있습니다. 게시할 준비가 되면 게시물을 posts 디렉터리에 배치할 수 있습니다.

### 설치

GUI는 `web` 디렉터리로 이동하여 `npm install`, `pnpm install` 또는 즐겨 사용하는 패키지 관리자를 사용하여 설치할 수 있습니다. 그런 다음 개발 서버를 실행하여 앱을 시작하기만 하면 됩니다.

_별도의 터미널에서 `fabric --serve` 명령으로 fabric을 실행해야 합니다._

**fabric 프로젝트 `web/` 디렉터리에서:**

```shell
npm run dev

## 또는 ##

pnpm run dev

## 또는 이에 상응하는 명령
```

### Streamlit UI

Streamlit 사용자 인터페이스를 실행하려면:

```bash
# 필요한 종속성 설치
pip install -r requirements.txt

# 또는 수동으로 종속성 설치
pip install streamlit pandas matplotlib seaborn numpy python-dotenv pyperclip

# Streamlit 앱 실행
streamlit run streamlit.py
```

Streamlit UI는 다음에 대한 사용자 친화적인 인터페이스를 제공합니다.

- 패턴 실행 및 연결
- 패턴 출력 관리
- 패턴 생성 및 편집
- 패턴 결과 분석

#### 클립보드 지원

Streamlit UI는 다양한 플랫폼에서 클립보드 작업을 지원합니다.

- **macOS**: `pbcopy` 및 `pbpaste` 사용 (내장)
- **Windows**: `pyperclip` 라이브러리 사용 (`pip install pyperclip`으로 설치)
- **Linux**: `xclip` 사용 (`sudo apt-get install xclip` 또는 배포판에 맞는 명령으로 설치)

## 메타

> [!NOTE]
> 영감과 기여를 해주신 다음 분들께 특별히 감사드립니다!

- _Jonathan Dunn_은 새로운 Go 버전과 GUI를 주도하는 등 프로젝트의 절대적인 MVP 개발자였습니다! 이 모든 것을 풀타임 의사로 일하면서 해냈습니다!
- _Caleb Sima_는 이 프로젝트를 공개 프로젝트로 만들지 여부에 대한 결정을 내리도록 저를 밀어붙였습니다.
- _Eugen Eisler_와 _Frederick Ros_는 Go 버전에 귀중한 기여를 했습니다.
- _David Peters_는 웹 인터페이스 작업에 기여했습니다.
- _Joel Parish_는 프로젝트의 Github 디렉터리 구조에 대한 매우 유용한 의견을 제시했습니다.
- _Joseph Thacker_는 `./config/fabric/` 디렉터리에 미리 만들어진 컨텍스트를 모든 패턴 쿼리에 추가하는 `-c` 컨텍스트 플래그 아이디어를 제시했습니다.
- _Jason Haddix_는 로컬 모델을 사용하여 콘텐츠를 필터링한 후 클라우드 모델로 보내는 스티치(연결된 패턴) 아이디어를 제시했습니다. 즉, `llama2`를 사용하여 고객 데이터를 정리한 후 분석을 위해 `gpt-4`로 보냅니다.
- _Andre Guerra_는 작업을 더 간단하고 유지 관리하기 쉽게 만드는 데 수많은 구성 요소로 도움을 주었습니다.

### 주요 기여자

<a href="https://github.com/danielmiessler"><img src="https://avatars.githubusercontent.com/u/50654?v=4" title="Daniel Miessler" width="50" height="50"></a>
<a href="https://github.com/xssdoctor"><img src="https://avatars.githubusercontent.com/u/9218431?v=4" title="Jonathan Dunn" width="50" height="50"></a>
<a href="https://github.com/sbehrens"><img src="https://avatars.githubusercontent.com/u/688589?v=4" title="Scott Behrens" width="50" height="50"></a>
<a href="https://github.com/agu3rra"><img src="https://avatars.githubusercontent.com/u/10410523?v=4" title="Andre Guerra" width="50" height="50"></a>

### 기여자

<a href="https://github.com/danielmiessler/fabric/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=danielmiessler/fabric" />
</a>

[contrib.rocks](https://contrib.rocks)로 만들었습니다.

`fabric`은 2024년 1월 <a href="https://danielmiessler.com/subscribe" target="_blank">Daniel Miessler</a>가 만들었습니다.
<br /><br />
<a href="https://twitter.com/intent/user?screen_name=danielmiessler">![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/danielmiessler)</a>
