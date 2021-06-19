---
title: Creating Wiki pages using Mark down
description: Demonstrates how wiki pages can be created
authors:
    - Mohammad Nadeem
date: 2020-11-25
---

## 1️⃣ Basics

Get started with [Markdown basics](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax){target=_blank} then move on to [advance concepts](https://guides.github.com/features/mastering-markdown/){target=_blank} .

Download the [cheat sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

Move on to learning [linking pages](https://www.mkdocs.org/user-guide/writing-your-docs/#linking-to-pages){target=_blank}

## 2️⃣ Components

> Note : Space place very critical role in Markdown.

### Tabs

Refer [this](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/){target=_blank} for more details.

#### Markup

```
  === "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

  === "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

```
#### Output

=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

### Tables 

Refer [this](https://squidfunk.github.io/mkdocs-material/reference/data-tables/){target=_blank} for more details

=== "Output"

    | Method      | Description                          |
    | ----------- | ------------------------------------ |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |

=== "Markdown"

    ```
    | Method      | Description                          |
    | ----------- | ------------------------------------ |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |
    ```

### Images

#### Example #1
=== "Output"

    ![Placeholder](https://dummyimage.com/600x400/eee/aaa){: align=left }

=== "Markdown"

    ```
       ![Placeholder](https://dummyimage.com/600x400/eee/aaa){: align=left }
    ```

#### Example #2

=== "Output"

    ![](../img/Octocat.png)   

=== "Markdown"

    ```
       ![](../img/Octocat.png)
    ```


### Task Lists

=== "Output"

    - [X] item 1
        * [X] item A
        * [ ] item B
            more text
            + [x] item a
            + [ ] item b
            + [x] item c
        * [X] item C
    - [ ] item 2
    - [ ] item 3
   

=== "Markdown"

    ```
       - [X] item 1
          * [X] item A
          * [ ] item B
              more text
              + [x] item a
              + [ ] item b
              + [x] item c
          * [X] item C
      - [ ] item 2
      - [ ] item 3
    ```


### Call outs

See [this](https://squidfunk.github.io/mkdocs-material/reference/admonitions/){target=_blank} for more details.


#### Success 


=== "Output"

    !!! success "optional explicit title within double quotes"
        Any number of other indented markdown elements.

        This is the second paragraph.

=== "Markdown"

    ```
    !!! success "optional explicit title within double quotes"
    Any number of other indented markdown elements.

    This is the second paragraph.
    ```


#### Note 

=== "Output"

    !!! note
        You should note that the title will be automatically capitalized.h.

=== "Markdown"

    ```
    !!! note
        You should note that the title will be automatically capitalized.
    ```

#### Danger 

=== "Output"

    !!! danger "Don't try this at home"
        ...

=== "Markdown"

    ```
    !!! danger "Don't try this at home"
        ...
    ```


#### Important 


=== "Output"

    !!! important ""
        This is important admonition box.

=== "Markdown"

    ```
    !!! important ""
        This is important admonition box.
    ```

#### Tip 

=== "Output"

    !!! tip "tip"
        This is tip admonition box.  

=== "Markdown"

    ```
    !!! tip "tip"
        This is tip admonition box.  
    ```


#### Warning 

=== "Output"

    !!! warning "warning"
        This is warning admonition box.

=== "Markdown"

    ```
    !!! warning "warning"
        This is warning admonition box. 
    ```

#### Error 


=== "Output"

    !!! error "error"
        This is an error admonition box. 

=== "Markdown"

    ```
    !!! error "error"
        This is an error admonition box. 
    ```

#### Info 


=== "Output"

    !!! info "info"
        This is an info admonition box. 

=== "Markdown"

    ```
    !!! info "info"
        This is an info admonition box. 
    ```



#### Quote  


=== "Output"

    !!! quote  "quote "
        This is an quote  admonition box. 

=== "Markdown"

    ```
    !!! quote  "quote "
        This is an quote admonition box. 
    ```

#### Example 


=== "Output"

    !!! example "example"
        This is an example admonition box. 

=== "Markdown"

    ```
    !!! example "example"
        This is an example admonition box. 
    ```

#### Question 


=== "Output"

    !!! question "question"
        This is an example admonition box. 

=== "Markdown"

    ```
    !!! question "question"
        This is an question admonition box. 
    ```

#### Failure 


=== "Output"

    !!! failure "failure"
        This is an failure admonition box. 

=== "Markdown"

    ```
    !!! failure "failure"
        This is an failure admonition box. 
    ```

#### Danger 


=== "Output"

    !!! danger "danger"
        This is an danger admonition box. 

=== "Markdown"

    ```
    !!! danger "danger"
        This is an danger admonition box. 
    ```

#### Bug 


=== "Output"

    !!! bug "bug"
        This is an bug admonition box. 

=== "Markdown"

    ```
    !!! bug "bug"
        This is an bug admonition box. 
    ```

#### Abstract 


=== "Output"

    !!! abstract "abstract"
        This is an abstract admonition box. 

=== "Markdown"

    ```
    !!! abstract "abstract"
        This is an abstract admonition box. 
    ```

### Details

Refer [this](https://facelessuser.github.io/pymdown-extensions/extensions/details/){target=_blank} for more details

#### Example #1

=== "Output"

    ??? success
        Content.

    ??? warning classes
        Content.

    ??? tip
        Content.

    ??? note classes
        Content.
    
    ??? example classes
        Content.
    
    ??? quote classes
        Content.
    
    ??? info classes
        Content.

    ??? question classes
        Content.

    ??? failure classes
        Content.

    ??? bug classes
        Content.
    
    ??? abstract classes
        Content.

=== "Markdown"

    ```
        ??? success
            Content.

        ??? warning classes
            Content.
            
        ??? tip
            Content.

        ??? note classes
            Content.

        ??? success
            Content.

        ??? example classes
            Content.

        ??? quote classes
            Content.

        ??? info classes
            Content.
            
        ??? question classes
            Content.

         ??? failure classes
             Content.

        ??? bug classes
            Content.
        
        ??? abstract classes
            Content.
    ```

#### Example #2

=== "Output"

    ??? optional-class "Summary"
        Here's some content.

    ??? multiple optional-class "Summary"
        Here's some content.

=== "Markdown"

    ```
        ??? optional-class "Summary"
            optional-class: Here's some content.

        ??? multiple optional-class "Summary"
            multiple class: Here's some content. 
    ```

#### Example #3

=== "Output"

    ???+ note default expanded
        Here's some content.

=== "Markdown"

    ```
        ???+ note default expanded
             Here's some content. 
    ```


### Progress Bar

Refer [this](https://facelessuser.github.io/pymdown-extensions/extensions/progressbar/){target=_blank} for more details

#### Example #1


=== "Output"

     [=0% "0%"]
     [=5% "5%"]
     [=25% "25%"]
     [=45% "45%"]
     [=65% "65%"]
     [=85% "85%"]
     [=100% "100%"]

=== "Markdown"

    ```
       [=0% "0%"]
       [=5% "5%"]
       [=25% "25%"]
       [=45% "45%"]
       [=65% "65%"]
       [=85% "85%"]
       [=100% "100%"] 
    ```

#### Example #2


=== "Output"

     [=1/10 "10%"]
     [=5%]
     [=25% "More than 25%"]
     [=100/100 'All set']

=== "Markdown"

    ```
       [=1/10 "10%"]
       [=5%]
       [=25% "More than 25%"]
       [=100/100 'All set'] 
    ```

#### Example #3

=== "Output"
     [=100% "100%"]{: .static .blue}
     [=85% "85%"]{: .static .lightcyan}
     [=100% "100%"]{: .static .darkcyan}
     [=85% "85%"]{: .static .verydarkcyan}
     [=85% "85%"]{: .static .blueviolet}
     [=100% "100%"]{: .static .bisque}
     [=85% "85%"]{: .static .green}
     [=85% "85%"]{: .static .darkgreen}
     [=100% "100%"]{: .static .orange}
     [=85% "85%"]{: .static .orangered}
     [=100% "100%"]{: .static .olivedrab}
     [=85% "85%"]{: .static .red}
     [=100% "100%"]{: .static .gray}
     [=100% "100%"]{: .static .grey}

=== "Markdown"

    ```
        [=100% "100%"]{: .static .blue}
        [=85% "85%"]{: .static .lightcyan}
        [=100% "100%"]{: .static .darkcyan}
        [=85% "85%"]{: .static .verydarkcyan}
        [=85% "85%"]{: .static .blueviolet}
        [=100% "100%"]{: .static .bisque}
        [=85% "85%"]{: .static .green}
        [=85% "85%"]{: .static .darkgreen}
        [=100% "100%"]{: .static .orange}
        [=85% "85%"]{: .static .orangered}
        [=100% "100%"]{: .static .olivedrab}
        [=85% "85%"]{: .static .red}
        [=100% "100%"]{: .static .gray}
        [=100% "100%"]{: .static .grey}
    ```


#### Example #4

=== "Output"

     [=85% "85%"]{: .candystripe}
     [=100% "100%"]{: .candystripe .candystripe-animate}

     [=0%]{: .thin}
     [=5%]{: .thin}
     [=25%]{: .thin}
     [=45%]{: .thin}
     [=65%]{: .thin}
     [=85%]{: .thin}
     [=100%]{: .thin}

=== "Markdown"

    ```
       [=85% "85%"]{: .candystripe}
       [=100% "100%"]{: .candystripe .candystripe-animate}

       [=0%]{: .thin}
       [=5%]{: .thin}
       [=25%]{: .thin}
       [=45%]{: .thin}
       [=65%]{: .thin}
       [=85%]{: .thin}
       [=100%]{: .thin} 
    ```

#### Example #5

=== "Output"
     [=91% "Going good"]{: .static .blue}
     [=85% "In progress"]{: .static .orange}
     [=100% "Blocked"]{: .static .red}
     [=100% "Not Started"]{: .static .grey}
     [=100% "Completed"]{: .static .darkgreen}     

=== "Markdown"

    ```
       [=91% "Going good"]{: .static .blue}
       [=85% "In progress"]{: .static .orange}
       [=100% "Blocked"]{: .static .red}
       [=100% "Not Started"]{: .static .grey}
       [=100% "Completed"]{: .static .darkgreen}  
    ```


## 3️⃣ References

### Markdown 💪
* [Github Markdown](https://guides.github.com/features/mastering-markdown/){target=_blank}
* [Mkdocs Writing your Docs](https://www.mkdocs.org/user-guide/writing-your-docs/){target=_blank}
* [Material for MKDocs](https://squidfunk.github.io/mkdocs-material/getting-started/){target=_blank}
* [pymdown-extensions](https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/){target=_blank}

### Emojis 😃
* [Emojis](https://emojipedia.org/nature/){target=_blank}
* [Github Markup Emojis](https://gist.github.com/rxaviers/7360908){target=_blank}
* [emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
* [style-digits](http://www.i2symbol.com/symbols/style-digits)

### Badges 📛
* [Badges](https://shields.io/){target=_blank}

### Drawings ✒️
* [mermaid js](https://mermaid-js.github.io/mermaid/#/flowchart){target=_blank}
* [mermaid plugin](https://github.com/fralau/mkdocs-mermaid2-plugin){target=_blank}

### Others 📒
* [Markdown Guide](https://www.markdownguide.org/tools/){target=_blank}
