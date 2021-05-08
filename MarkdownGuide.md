# Markdown Guide  
소프트웨어공학 Markdown README.md 작성

# CHAPTER 1. 머리글  
1. \# 뒤에 공백 후 문장을 작성한다.  
2. \#의 개수가 적을수록 글씨의 크기가 크다.(단 1~6개까지만 지원함)  
3. 예시  
    1. 입력  
        - `# Heading level 1`  
        - `## Heading level 2`  
        - `### Heading level 3`  
        - `##### Heading level 4`  
        - `##### Heading level 5`  
        - `###### Heading level 6`  
    2. 출력  
        # Heading level 1
        ## Heading level 2
        ### Heading level 3
        #### Heading level 4
        ##### Heading level 5
        ###### Heading level 6

4. Heading level 1과 2는 다른 표현방식이 존재한다.
    1. 입력  
        - `Heading level 1`  
          `==================`
        - `# Heading level 1` 과 같다.  
    2. 출력  

        Heading level 1
        ===============
    

    3. 입력  
        - `Heading level 2`  
        `------------------`
        - `## Heading level 2` 과 같다.  
    4. 출력  

        Heading level 2
        ---------------
5. \# 뒤에 공백이 반드시 들어가야한다.  
    - `#Heading` (X)
    - `# Heading` (O)

# CHAPTER 2. 단락  
1. 단락을 만들기 위해서는 빈 줄을 사용하여 하나 이상의 텍스트 줄을 분리한다.
2. 예시
    - I really like using Markdown.

      I think I'll use it to format all of my documents from now on.
3. 단, 단락을 만들 때 목록을 만든 것이 아니면 들여쓰기를 하지 말 것.

# CHAPTER 3. 줄 바꿈  
1. 줄을 바꾸기 위해서는 문장 끝에 공백을 두 개 이상 입력한다.
2. 공백을 두 개 이상 입력하지 않으면 그대로 문장이 이어서 출력된다.
3. 예시
    - This is the first line.__  
      And this is the second line.
    - This is the first line.
      And this is also the first line.

# CHAPTER 4. 굵게 강조  
1. 굵게 강조하고자 하는 단어나 구 전후에 공백 없이 두 개의 **\*** 혹은 __\___ 을 추가한다.
2. 예시
    1. 입력  
        - `I just love **bold text**`.
        - `I just love __bold text__`.  
    2. 출력  
        - I just love **bold text**. 
        - I just love __bold text__. 
3. 단, 굵게 강조할 양 옆이 띄어쓰기가 없다면 \*만 사용할 수 있다.
    - `Love**is**bold.` (O)
    - `Love__is__bold.` (X)

# CHAPTER 5. 기울이기 강조  
1. 기울여서 강조하고자 하는 단어나 구 전후에 공백 없이 한 개의 *\** 혹은 _\__ 을 추가한다.
2. 예시
    1. 입력  
        - `Italicized text is the *cat's meow*`.
        - `Italicized text is the _cat's meow_`.
    2. 출력  
        - Italicized text is the *cat's meow*. 
        - Italicized text is the _cat's meow_.  
3. 단, 기울여 강조할 양 옆이 띄어쓰기가 없다면 \*만 사용할 수 있다.
    - `A*cat*meow.` (O)
    - `A_cat_meow.` (X)

# CHAPTER 6. 굵게 기울이기 강조  
1. 굵게 동시에 기울여서 강조하고자 하는 단어나 구 전후에 공백 없이 세 개의 **\*** 혹은 __\___ 을 추가한다.
2. \*와 \_ 을 섞어서 사용이 가능하다.
3. 예시
    1. 입력  
        - `This text is ***really important***`.
        - `This text is ___really important___`.
        - `This text is __*really important*__`.
        - `This text is **_really important_**`.
    2. 출력  
        - This text is ***really important***.
        - This text is ___really important___.  
        - This text is __*really important*__.  
        - This text is **_really important_**.  
      
4. 단, 굵게 동시에 기울여 강조할 양 옆이 띄어쓰기가 없다면 \*만 사용할 수 있다.
    - `This is really***very***important text.` (O)
    - `This is really___very___important text.` (X)

# CHAPTER 7. 블록  
1. \> 을 사용해 단락 앞에 블록을 추가한다.
2. 예시
    1. 입력  
        - `> Dorothy followed her through many of the beautiful rooms in her castle.`
    2. 출력  
        > Dorothy followed her through many of the beautiful rooms in her castle.  

3. \>을 여러번 사용하면 블록을 중첩할 수 있다.
    1. 입력  
        - `> Dorothy followed her through many of the beautiful rooms in her castle.`  
        `>`  
        `>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.`
    2. 출력  
        > Dorothy followed her through many of the beautiful rooms in her castle.
        >
        >> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

    
4. 다른 서식 요소와 블록을 중첩할 수 있다. (ex. \-, \+ ...)

# CHAPTER 8. 목록  
1. 숫자 뒤에 마침표를 추가해 순서있는 목록을 만들 수 있다.
2. 목록의 첫 숫자가 1이면 뒤의 목록의 번호는 상관없다.
3. 예시
    1. 입력
        - `1. First item`  
          `2. Second item`  
          `3. Third item` 
           
        - `1. First item`  
          `1. Second item`  
          `1. Third item`  

        - `1. First item`  
          `3. Second item`  
          `2. Third item`  
    2. 출력  
        - 1. First item
          2. Second item
          3. Third item
        - 1. First item
          1. Second item
          1. Third item
        - 1. First item
          3. Second item
          2. Third item
4. 들여쓰기를 통해 목록을 중첩할 수 있다.
    1. 입력  
        - `1. First item`  
          `2. Second item`  
                  `____1. Indented item`  
                  `____2. Indented item`  
          `3. Third item`  
          //들여쓰기가 되지 않아 임의로 밑줄 입력
    2. 출력 
        - 1. First item
          2. Second item
              1. Indented item
              2. Indented item
          3. Third item
5. \-, \*, \+ 를 사용해 순서 없는 목록을 만들 수 있다. 마찬가지로 중첩이 가능하다.
    1. 입력
        - `- First item`  
          `- Second item`  
          `- Third item`
        - `* First item`  
          `* Second item`  
          `* Third item`
        - `+ First item`  
          `+ Second item`  
          `+ Third item`
    2. 출력
        - - First item  
          - Second item  
          - Third item
        - * First item  
          * Second item  
          * Third item
        - + First item  
          + Second item  
          + Third item
6. \-. \*, \+ 를 혼합하기보다는 일치해서 사용하는 것이 좋다.
7. 블록과 목록을 혼합하여 사용이 가능하다.

# CHAPTER 9. 코드블록  
1. 코드블록은 4개의 공백 또는 하나의 탭을 들여쓰기 한다. 목록에 있을 때에는 8개의 공백 또는 두 개의 탭을 들여쓰기 한다.
2. 예시
    1. 입력  
        - `1.  Open the file.`  
          `2.  Find the following code block on line 21:`  

          `__<html>`  
          `____<head>`  
          `______<title>Test</title>`  
          `____</head>`  

          `3.  Update the title to match the name of your website.`  
    2. 출력
        - 1.  Open the file.
          2.  Find the following code block on line 21:

                  <html>
                    <head>
                      <title>Test</title>
                    </head>

          3.  Update the title to match the name of your website.
3. 단어나 구를 코드로 나타내려면 \`를 나타내고자 하는 코드의 문장 전후에 입력한다.
4. 예시
    1. 입력  
        - ``At the command prompt, type `nano`.``
    2. 출력  
        - At the command prompt, type `nano`.
5. 코드로 나타내려는 단어나 문구에 \`가 하나 이상 포함되어 있다면 \`를 두번 사용하여 표현할 수 있다.
6. 예시
    1. 입력  
        - \`\```Use `code` in your Markdown file.``\`\`
    2. 출력  
        - ``Use `code` in your Markdown file.``

# CHAPTER 10. 수평선  
1. \*, \-, \_를 세 개 이상 사용하면 줄이 생성된다.
2. 예시  
    1. 입력
        - \*\*\*
        - \-\-\-
        - \_\_\_
    2. 출력

        - ***

        - 세 종류 모두 동일한 줄이 생성됨.
3. 수평선 전후에 빈 줄을 놓아야 한다.

# CHAPTER 11. 링크  
1. 괄호 안에 표시할 텍스트를 넣고, 그 옆의 괄호 안에 URL을 넣는다.
2. 예시
    1. 입력
        - `Link: [Google](https://google.com)`
    2. 출력
        - Link : [Google](https://google.com)
3. URL이 포함된 괄호에서 URL 옆에 텍스트를 작성하고 ""로 둘러싸면 링크를 마우스로 가져가면 설명이 나온다.
4. 예시
    1. 입력
        - `Link: [Google](https://google.com "구글주소")`
    2. 출력
        - Link : [Google](https://google.com "구글주소")
5. URL과 이메일 주소를 링크로 빠르게 바꾸려면 각진 괄호를 사용한다.
6. 예시
    1. 입력
        - `<https://google.com>`
        - `<address@soongsil.ac.kr>`
    2. 출력
        - <https://google.com>
        - <address@soongsil.ac.kr>
7. 링크를 굵게 또는 기울여서 강조할 수 있다.
8. 링크를 코드로 나타내려면 괄호에 \`를 추가한다.

# CHAPTER 12. 이미지  
1. 이미지를 추가하려면 \!, 뒤에 괄호에 표시할 텍스트, 이미지의 URL을 추가한다.
2. 예시
    1. 입력
        - `![숭실대학교 로고](https://ssu.ac.kr/wp-content/uploads/2019/04/cymbal_mark.png)`
    2. 출력
        - ![숭실대학교 로고](https://ssu.ac.kr/wp-content/uploads/2019/04/cymbal_mark.png)
3. 이미지를 링크에 추가하려면 []를 두르고 괄호안에 링크를 넣어 추가한다.
4. 예시
    1. 입력
        - `[![숭실대학교 로고](https://ssu.ac.kr/wp-content/uploads/2019/04/cymbal_mark.png "Symbol of Soongsil University")](https://ssu.ac.kr/)`
    2. 출력
        - [![숭실대학교 로고](https://ssu.ac.kr/wp-content/uploads/2019/04/cymbal_mark.png "Symbol of Soongsil University")](https://ssu.ac.kr/)

# CHAPTER 13. 이스케이프 문자  
1. 백슬래시 \\를 사용하여 명령어로 쓰이는 문자들을 출력할 수 있다.
2. 이스케이프 문자 종류
    - \\
    - \`
    - \*
    - \_
    - \{\}
    - \[\]
    - \[\]
    - \<\>
    - \(\)
    - \#
    - \+
    - \-
    - \.
    - \!
    - \|

# Extra Chapter. My Github
1. GitHub Repository URL : [SWEngineering](https://github.com/soheeee217/SWEngineering.git)
