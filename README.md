# webpack
webpack config detail

## 1. Webpack
- 모듈등의 파일들을 묶음 파일로 변경함(js, css 등 static assets)
- dependency graph를 이용하여 mapping 하여 변경함

### 6 가지 주요 사항: webpack runs on Node.js version 8.x and higher.
- Entry: 시작 지점(string, array)
   -> usage: entry: string | [string]
- Output: 최종 파일 생성 지점
- Loaders: 변환된 파일 지정하여, 변경할때 사용할 로더를 정의함
           특정 유형의 파일을 변경함
    module{
        rules: [
            {
                // 내부에 사용할 모듈 로더 정의함
                test: /\.js$/,
                use: 'babel-loader'
            }
        ]
    }
- Plugins: Loader와 달리 전체 Webpack의 번들 최적화, 환경 변수 주입등 전반적인 내용을 변경 처리함
- Mode: Webpack의 최적화를 사용 할 수 있음(production, development)
- Browser Compatibility: Webpack 지원(IE9 이상, ES5 지원)
                         추가 지원은 Polyfill등을 사용해야함
