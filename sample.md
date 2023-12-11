# Markdown Plus

Markdown Plus ("M+" or "mdp" for short) is a markdown editor with extra features.

## Apps

We currently **_don't_** accept donations.
The best way to support our development is to buy our apps.

### Markdown Plus

<a href="javascript:;"><img src="./icon.png" height="64px"/></a>
[Markdown Plus](javascript:;) is available for both OS X and Windows. You get every feature of the web version plus lots of advanced features.

### Markdown Mate

<a href="javascript:;"><img src="./icon.png" height="64px"/></a>
[Markdown Mate](javascript:;) is a markdown previewer, it's not going to replace your favorite editor but handles everything about markdown.

::: success
We provide email support to those who have purchased the apps: **service@TTTTT.com**
:::

---

# Table of Contents

[toc]

Note: Only `h2` and `h3` are shown in toc.

## Mastering Markdown

Markdown allows you to write using an easy-to-read, easy-to-write plain text format, which then converts to valid HTML for viewing.

[Mastering Markdown Guide](https://guides.github.com/features/mastering-markdown/).

## ~~strikethrough~~

## ++insert++

## ==mark==

## Subscript: H~2~O

You can also use inline math: `$H_2O$`

## Superscript: 29^th^

You can also use inline math: `$29^{th}$`

## Emoji: :panda_face: :sparkles: :camel: :boom: :pig:

[Emoji Cheat Sheet](http://www.emoji-cheat-sheet.com/)

## Fontawesome: :fa-cab: :fa-flag: :fa-bicycle: :fa-leaf: :fa-heart:

[All the Font Awesome icons](http://fontawesome.io/icons/)

## `print 'hello code'`

    evens = [1, 2, 3, 4, 5].collect do |item|
      item * 2
    end

```javascript
$(document).ready(() => {
    $("pre code").each((i, block) => {
        hljs.highlightBlock(block);
    });
});
```

[Code Formatting](https://help.github.com/articles/markdown-basics/#code-formatting)

## Tables and alignment

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |

| Left-Aligned | Center Aligned  | Right Aligned |
| :----------- | :-------------: | ------------: |
| col 3 is     | some wordy text |        \$1600 |
| col 2 is     |    centered     |          \$12 |

[Table Syntax](https://help.github.com/articles/github-flavored-markdown/#tables)

## Task list

-   [ ] a bigger project
    -   [x] first subtask
    -   [x] follow up subtask
    -   [ ] final subtask
-   [ ] a separate task

[Task List Syntax](https://help.github.com/articles/writing-on-github/#task-lists)

## Abbreviation

Markup is based on [php markdown extra](https://michelf.ca/projects/php-markdown/extra/#abbr) definition, but without multiline support:

_[HTML]: Hyper Text Markup Language
_[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.

## Footnote

Here is a footnote reference,[^1] and another.[^longnote]

[^1]: Here is the footnote.
[^longnote]: Here's one with multiple blocks.

    Subsequent paragraphs are indented to show that they

belong to the previous footnote.

Here is an inline note.^[Inlines notes are easier to write, since
you don't have to pick an identifier and move down to type the
note.]

[Footnote Syntax](http://pandoc.org/README.html#footnotes)

## Mathematical formula `$y = x^2$`

Inline math: `$\dfrac{ \tfrac{1}{2}[1-(\tfrac{1}{2})^n] }{ 1-\tfrac{1}{2} } = s_n$`.

Math block:

```katex
\oint_C x^3\, dx + 4y^2\, dy

2 = \left(
 \frac{\left(3-x\right) \times 2}{3-x}
 \right)

\sum_{m=1}^\infty\sum_{n=1}^\infty\frac{m^2\,n}
 {3^m\left(m\,3^n+n\,3^m\right)}

\phi_n(\kappa) =
 \frac{1}{4\pi^2\kappa^2} \int_0^\infty
 \frac{\sin(\kappa R)}{\kappa R}
 \frac{\partial}{\partial R}
 \left[R^2\frac{\partial D_n(R)}{\partial R}\right]\,dR
```

[Mathematical Formula Syntax](http://meta.wikimedia.org/wiki/Help:Displaying_a_formula)

## AsciiMath

Inline AsciiMath: `@(1/2[1-(1/2)^n])/(1-(1/2))=s_n@`

```AsciiMath
oint_Cx^3 dx+4y^2 dy

2=(((3-x)xx2)/(3-x))

sum_(m=1)^oosum_(n=1)^oo(m^2 n)/(3^m(m3^n+n3^m)
```

```ASCIIMath
phi_n(kappa) = 1/(4pi^2 kappa^2)
 int_0^oo (sin(kappa R))/(kappa R)
 del/(del R)
[R^2 (del D_n (R))/(del R)] del R
```

[AsciiMath Documentation](http://asciimath.org/)

## Graphviz

### Graphviz 思维导图

```graphviz
digraph g {
	rankdir=LR  //方向左右
	dot语言->{简介,语法,示例}
	dot语言[shape=box,fontcolor=red]
	简介[color=red]
	语法[color=green]
	示例[color=blue]
	简介->{开源免费,UML绘图,导出svg}
	语法->{"digraph","graph"}
	"digraph"->导向图[label=可以制作带方向的导图]
	"graph"->无向图[label=可以制作不带方向的导图]
}
```


### Graphviz 流程图

```graphviz
digraph G {

	subgraph cluster_0 {
		style=filled;
		color=lightgrey;
		node [style=filled,color=white];
		a0 -> a1 -> a2 -> a3;
		label = "process #1";
	}

	subgraph cluster_1 {
		node [style=filled];
		b0 -> b1 -> b2 -> b3;
		label = "process #2";
		color=blue
	}
	start -> a0;
	start -> b0;
	a1 -> b3;
	b2 -> a3;
	a3 -> a0;
	a3 -> end;
	b3 -> end;

	start [shape=Mdiamond];
	end [shape=Msquare];
}
```

### Graphviz action 图

```graphviz
digraph action {
    node [shape = record,height=.1];

    node0 [label = "<head> head|<body> body|<foot> foot", height=.5]
    node2 [shape = box label="mind"]

    node0:head:n -> node2:n [label = "n"]
    node0:head:ne -> node2:ne [label = "ne"]
    node0:head:e -> node2:e [label = "e"]
    node0:head:se -> node2:se [label = "se"]
    node0:head:s -> node2:s [label = "s"]
    node0:head:sw -> node2:sw [label = "sw"]
    node0:head:w -> node2:w [label = "w"]
    node0:head:nw -> node2:nw [label = "nw"]
    node0:head:c -> node2:c [label = "c"]
    node0:head:_ -> node2:_ [label = "_"]

    node0:body[style=filled color=lightblue]
}
```

### Graphviz TCP IP 状态流程图

```graphviz
digraph {
    compound=true
    fontsize=10
    margin="0,0"
    ranksep = .75
    nodesep = .65

    node [shape=Mrecord fontname="Inconsolata, Consolas", fontsize=12, penwidth=0.5]
    edge [fontname="Inconsolata, Consolas", fontsize=10, arrowhead=normal]


    "TCP/IP State Transition" [shape = "plaintext", fontsize = 16]

    // now start server state transition
    "CLOSED" -> "LISTEN" [style = blod, label = "应用：被动打开\n发送：<无>"];
    "LISTEN" -> "SENT_REVD" [style = blod, label = "接收：SYN\n发送：SYN,ACK"]
    "SENT_REVD" -> "ESTABLISHED" [style = blod, label = "接收：ACK\n发送：<无>", weight = 20]
    "ESTABLISHED" -> "CLOSE_WAIT" [style = blod, label = "接收：FIN\n发送：ACK", weight = 20]

    subgraph cluster_passive_close {
        style = dotted
        margin = 10

        passive_close [shape = plaintext, label = "被动关闭", fontsize = 14]

        "CLOSE_WAIT" -> "LAST_ACK" [style = blod, label = "应用：关闭\n发送：FIN", weight = 10]
    }
    "LAST_ACK" -> "CLOSED" [style = blod, label = "接收：ACK\n发送：<无>"]

    // now start client state transition
    "CLOSED" -> "SYN_SENT" [style = dashed, label = "应用：主动打开\n发送：SYN"];
    "SYN_SENT" -> "ESTABLISHED" [style = dashed, label = "接收：SYN,ACK\n发送：ACK", weight = 25]
    "SYN_SENT" -> "SENT_REVD" [style = dotted, label = "接收：SYN\n发送：SYN,ACK\n同时打开"]
    "ESTABLISHED" -> "FIN_WAIT_1" [style = dashed, label = "应用：关闭\n发送：FIN", weight = 20]

    subgraph cluster_active_close {
        style = dotted
        margin = 10

        active_open [shape = plaintext, label = "主动关闭", fontsize = 14]

        "FIN_WAIT_1" -> "FIN_WAIT_2" [style = dashed, label = "接收：ACK\n发送：<无>"]
        "FIN_WAIT_2" -> "TIME_WAIT" [style = dashed, label = "接收：FIN\n发送：ACK"]
        "FIN_WAIT_1" -> "CLOSING" [style = dotted, label = "接收：ACK\n发送：<无>"]
        "FIN_WAIT_1" -> "TIME_WAIT" [style = dotted, label = "接收：SYN,ACK\n发送：ACK"]
        "CLOSING" -> "TIME_WAIT" [style = dotted]
    }

    "TIME_WAIT" -> "CLOSED" [style = dashed, label = "2MSL超时"]
}
```

### Graphviz epoll 相关数据结构及关系

```graphviz
digraph rankdot {
    compound=true
    margin="0,0"
    ranksep = .75
    nodesep = 1
    pad = .5
    rankdir = LR

    node [shape=record, charset = "UTF-8" fontname="Microsoft YaHei", fontsize=14]
    edge [style = dashed, charset = "UTF-8" fontname="Microsoft YaHei", fontsize=11]

    epoll [shape = plaintext, label = "epoll 相关结构及部分关系"]

    eventpoll [
        color = cornflowerblue,
        label = "<eventpoll> struct \n eventpoll |
            <lock> spinlock_t lock; |
            <mutex> struct mutex mtx; |
            <wq> wait_queue_head_t wq; |
            <poll_wait> wait_queue_head_t poll_wait; |
            <rdllist> struct list_head rdllist; |
            <ovflist> struct epitem *ovflist; |
            <rbr> struct rb_root_cached rbr; |
            <ws> struct wakeup_source *ws; |
            <user> struct user_struct *user; |
            <file> struct file *file; |
            <visited> int visited; |
            <visited_list_link> struct list_head visited_list_link;"
    ]

    epitem [
        color = sienna,
        label = "<epitem> struct \n epitem  |
            <rb>struct rb_node rbn;\nstruct rcu_head rcu; |
            <rdllink> struct list_head rdllink; |
            <next> struct epitem *next; |
            <ffd> struct epoll_filefd ffd; |
            <nwait> int nwait; |
            <pwqlist> struct list_head pwqlist; |
            <ep> struct eventpoll *ep; |
            <fllink> struct list_head fllink; |
            <ws> struct wakeup_source __rcu *ws; |
            <event> struct epoll_event event;"
    ]

    epitem2 [
        color = sienna,
        label = "<epitem> struct \n epitem |
            <rb>struct rb_node rbn;\nstruct rcu_head rcu; |
            <rdllink> struct list_head rdllink; |
            <next> struct epitem *next; |
            <ep> struct eventpoll *ep; |
             ··· |
             ··· "
    ]

    eppoll_entry [
        color = darkviolet,
        label = "<entry> struct \n eppoll_entry |
            <llink> struct list_head llink; |
            <base> struct epitem *base; |
            <wait> wait_queue_entry_t wait; |
            <whead> wait_queue_head_t *whead;"
    ]

    epitem:ep -> eventpoll:se [color = sienna]
    epitem2:ep -> eventpoll:se [color = sienna]
    eventpoll:ovflist -> epitem:next -> epitem2:next [color = cornflowerblue]
    eventpoll:rdllist -> epitem:rdllink -> epitem2:rdllink [dir = both]
    eppoll_entry:llink -> epitem:pwqlist [color = darkviolet]
    eppoll_entry:base -> epitem:nw  [color = darkviolet]
}
```

---

## mermaid charts

### Flowchart

```mermaid
graph TD
A[Christmas] -->|Get money| B(Go shopping)
B --> C{Let me think}
C -->|One| D[Laptop]
C -->|Two| E[iPhone]
C -->|Three| F[Car]
```

[Flowchart Syntax](http://knsv.github.io/mermaid/#flowcharts-basic-syntax)

::: warning
Adding many flowcharts will slow down the editor.
:::

### Sequence diagram

```mermaid
sequenceDiagram
loop every day
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
end
```

[Sequence Diagram Syntax](http://knsv.github.io/mermaid/#sequence-diagrams)

::: warning
Adding many sequence diagrams will slow down the editor.
:::

### Gantt diagram

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d

section Critical tasks
Completed task in the critical line :crit, done, 2014-01-06,24h
Implement parser and jison          :crit, done, after des1, 2d
Create tests for parser             :crit, active, 3d
Future task in critical line        :crit, 5d
Create tests for renderer           :2d
Add to mermaid                      :1d

section Documentation
Describe gantt syntax               :active, a1, after des1, 3d
Add gantt diagram to demo page      :after a1  , 20h
Add another diagram to demo page    :doc1, after a1  , 48h

section Last section
Describe gantt syntax               :after doc1, 3d
Add gantt diagram to demo page      : 20h
Add another diagram to demo page    : 48h
```

[Gantt Diagram Syntax](http://knsv.github.io/mermaid/#gant-diagrams)

::: warning
Adding many gantt diagrams will slow down the editor.
:::

### Class diagram

```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

Class diagram is powered by [mermaid](https://github.com/knsv/mermaid).

::: warning
Adding many class diagrams will slow down the editor.
:::

## Custom Container

Markup is similar to fenced code blocks. Valid container types are `success`, `info`, `warning` and `danger`.

::: info
You have new mail.
:::

::: danger
Staying up all night is bad for health.
:::

## Definition list

Term 1
~ Definition 1

Term 2
~ Definition 2a
~ Definition 2b

[Definition List Syntax](http://pandoc.org/README.html#definition-lists)

## HTML

If you find the markdown syntax too limited, you can try some <span style="color: blue;">HTML<span>:

<p style="text-align:center;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png"/></p>

<a href="javascript:;" target="_blank"><img style="position: absolute; top: 0; right: 0; border: 0;" src="http://aral.github.com/fork-me-on-github-retina-ribbons/right-green.png" alt="Fork me on GitHub"></a>

## Charts

[Documentation for charts](http://www.chartjs.org/docs/)

### Line Chart

```chart
{
  "type": "line",
  "data": {
    "labels": [
      "January",
      "February",
      "March",
      "April",
      "May",
      "June",
      "July"
    ],
    "datasets": [
      {
        "label": "# of bugs",
        "fill": false,
        "lineTension": 0.1,
        "backgroundColor": "rgba(75,192,192,0.4)",
        "borderColor": "rgba(75,192,192,1)",
        "borderCapStyle": "butt",
        "borderDash": [],
        "borderDashOffset": 0,
        "borderJoinStyle": "miter",
        "pointBorderColor": "rgba(75,192,192,1)",
        "pointBackgroundColor": "#fff",
        "pointBorderWidth": 1,
        "pointHoverRadius": 5,
        "pointHoverBackgroundColor": "rgba(75,192,192,1)",
        "pointHoverBorderColor": "rgba(220,220,220,1)",
        "pointHoverBorderWidth": 2,
        "pointRadius": 1,
        "pointHitRadius": 10,
        "data": [
          65,
          59,
          80,
          81,
          56,
          55,
          40
        ],
        "spanGaps": false
      }
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Line Chart](http://www.chartjs.org/docs/#line-chart)

### Bar Chart

```chart
{
  "type": "bar",
  "data": {
  "labels": [
    "Red",
    "Blue",
    "Yellow",
    "Green",
    "Purple",
    "Orange"
  ],
  "datasets": [
    {
    "label": "# of Votes",
    "data": [
      12,
      19,
      3,
      5,
      2,
      3
    ],
    "backgroundColor": [
      "rgba(255, 99, 132, 0.2)",
      "rgba(54, 162, 235, 0.2)",
      "rgba(255, 206, 86, 0.2)",
      "rgba(75, 192, 192, 0.2)",
      "rgba(153, 102, 255, 0.2)",
      "rgba(255, 159, 64, 0.2)"
    ],
    "borderColor": [
      "rgba(255,99,132,1)",
      "rgba(54, 162, 235, 1)",
      "rgba(255, 206, 86, 1)",
      "rgba(75, 192, 192, 1)",
      "rgba(153, 102, 255, 1)",
      "rgba(255, 159, 64, 1)"
    ],
    "borderWidth": 1
    }
  ]
  },
  "options": {}
}
```

<br/>

[Documentation for Bar Chart](http://www.chartjs.org/docs/#bar-chart)

### Radar Chart

```chart
{
  "type": "radar",
  "data": {
    "labels": [
      "Eating",
      "Drinking",
      "Sleeping",
      "Designing",
      "Coding",
      "Cycling",
      "Running"
    ],
    "datasets": [
      {
        "label": "My First dataset",
        "backgroundColor": "rgba(179,181,198,0.2)",
        "borderColor": "rgba(179,181,198,1)",
        "pointBackgroundColor": "rgba(179,181,198,1)",
        "pointBorderColor": "#fff",
        "pointHoverBackgroundColor": "#fff",
        "pointHoverBorderColor": "rgba(179,181,198,1)",
        "data": [
          65,
          59,
          90,
          81,
          56,
          55,
          40
        ]
      },
      {
        "label": "My Second dataset",
        "backgroundColor": "rgba(255,99,132,0.2)",
        "borderColor": "rgba(255,99,132,1)",
        "pointBackgroundColor": "rgba(255,99,132,1)",
        "pointBorderColor": "#fff",
        "pointHoverBackgroundColor": "#fff",
        "pointHoverBorderColor": "rgba(255,99,132,1)",
        "data": [
          28,
          48,
          40,
          19,
          96,
          27,
          100
        ]
      }
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Radar Chart](http://www.chartjs.org/docs/#radar-chart)

### Polar Area Chart

```chart
{
  "type": "polarArea",
  "data": {
    "datasets": [
      {
        "data": [
          11,
          16,
          7,
          3,
          14
        ],
        "backgroundColor": [
          "#FF6384",
          "#4BC0C0",
          "#FFCE56",
          "#E7E9ED",
          "#36A2EB"
        ],
        "label": "My dataset"
      }
    ],
    "labels": [
      "Red",
      "Green",
      "Yellow",
      "Grey",
      "Blue"
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Polar Area Chart](http://www.chartjs.org/docs/#polar-area-chart)

### Pie Chart

```chart
{
  "type": "pie",
  "data": {
    "labels": [
      "Red",
      "Blue",
      "Yellow"
    ],
    "datasets": [
      {
        "data": [
          300,
          50,
          100
        ],
        "backgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ],
        "hoverBackgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ]
      }
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Pie Chart](http://www.chartjs.org/docs/#doughnut-pie-chart)

### Doughnut Chart

```chart
{
  "type": "doughnut",
  "data": {
    "labels": [
      "Red",
      "Blue",
      "Yellow"
    ],
    "datasets": [
      {
        "data": [
          300,
          50,
          100
        ],
        "backgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ],
        "hoverBackgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ]
      }
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Doughnut Chart](http://www.chartjs.org/docs/#doughnut-pie-chart)

### Bubble Chart

```chart
{
  "type": "bubble",
  "data": {
    "datasets": [
      {
        "label": "First Dataset",
        "data": [
          {
            "x": 20,
            "y": 30,
            "r": 15
          },
          {
            "x": 40,
            "y": 10,
            "r": 10
          }
        ],
        "backgroundColor": "#FF6384",
        "hoverBackgroundColor": "#FF6384"
      }
    ]
  },
  "options": {}
}
```

<br/>

[Documentation for Bubble Chart](http://www.chartjs.org/docs/#bubble-chart)
