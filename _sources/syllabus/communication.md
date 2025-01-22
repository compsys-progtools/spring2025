---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---




# Office Hours & Communication



```{code-cell}
:tags: ["remove-input"]

import pandas as pd
from IPython.display import display, Markdown, HTML
pd.set_option('display.max_colwidth', 0)
# df = pd.read_csv('../_data/communication.csv')

help_df = pd.read_csv('../_data/help_hours.csv')
```

## Announcements

Announcements will be made via {term}`GitHub` Release. You can view them [online in the releases page](https://github.com/compsys-progtools/spring2025/releases) or you can get notifications by watching the {term}`repository`, choosing "Releases" under custom [see GitHub docs for instructions with screenshots](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#configuring-your-watch-settings-for-an-individual-repository). You can choose {term}`GitHub` only or e-mail notificaiton [from the notification settings page](https://github.com/settings/notifications)

```{warning}
For the first week announcements will be made by BrightSpace too, but after that, all course activities will be only on GitHub. 
```


````{admonition} Sign up to watch
:class: community, dropdown

Watch the repo and then, after the first class, [claim a community badge](community-process) for doing so, using a link to these instructions as the "contribution" like follows.   
```
- [watched the repo as per announcements](https://compsys-progtools.github.io/spring2025/syllabus/communication.html#announcements) 
```
put this on a {term}`branch` called `watch_community_badge` and title your PR "Community-Watch" 
````

## Help Hours


```{code-cell}
:tags: ["remove-input"]

help_df.style.hide(axis="index")
``` 

Online office hours locations and appointment links for alternative times are linked on the [GitHub Organization Page](https://github.com/compsys-progtools)

```{important}
You can only see them if you are a "member". To join, make sure that you have completed Lab 0. 
```

<!-- 
## Getting Help 

- E-mail the instructor and TAs: `cscsystools-help-group@uri.edu`
- Post an issue to the course website
-  -->

<!--
Online office hours locations are linked in the #help channel on slack
We have several different ways to communicate in this course. This section summarizes them -->

<!--
## To reach out, By usage

```{code-cell}
:tags: ["remove-input"]

df = df[['usage','platform','area','note']]
display(HTML(df.style.hide_index()._repr_html_()))
```

```{note}
e-mail is last because it's not collaborative; other platforms allow us (Proessor + TAs) to collaborate on who responds to things more easily.
```

## By Platform

```{code-cell}
:tags: ["remove-input"]

for platform, data in df.groupby('platform'):
    display(HTML('<h3> Use '+ platform + ' for </h3>'))
    display(HTML(data.drop(columns='platform').style.hide_index()._repr_html_()))

``` 
-->

## Tips

```{admonition} TLDR
:class: community

Contribute a TLDR set of tabs or mermaid visual to this section for a community badge. 
```

### For assignment help

- use the badge issue for comments and @ mention instructors 
- **send in advance, leave time for a response** 
- **always** use issues in your repo for content directly related to assignments.  If you {term}`push` your partial work to the {term}`repository` and then open an {term}`issue`, we can see your work and your question at the same time and download it to run it if we need to debug something
- use issues or discussions for questions about this syllabus or class notes. At the top right there's a {term}`GitHub` logo {fa}`github` that allows you to open a {term}`issue` (for a question) or suggest an edit (eg if you think there's a tpo or you find an additional helpful resource related to something)


```{note}
I check e-mail/github a small number of times per day, during work hours, almost exclusively. You might see me post to this site, post to BrightSpace, or comment on your assignments outside of my normal working hours, but I will not reliably see emails that arrive during those hours. This means that it is important to start assignments early.
```



```{admonition} Should you e-mail your work? 
:class: anchor,dropdown

No, request a {term}`pull request` review or make an {term}`issue` if you are stuck
```
