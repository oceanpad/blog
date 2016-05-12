---
title: play! Framework I18n
date: 2016-05-12 08:31:58
tags:
---
i18n = Internationalization: i, then 18 letters, then n
l10n = Localization: l, then 10 letters, then n
<!--more-->
Internationalization is important to this world's website and applications.
Play! Framework provide good I18n interface, you can use I18n to specify your language easily.

#### add config to application.conf
```
play.i18n.langs = [ "en", "en-US", "fr" ]
```

#### add messages.xx files to conf/ folder
messages.ja
messages.cn
messages.en
...
```
messages.en:
info.error=You aren''t logged in!
example.formatting=When using MessageFormat, '''{0}''' is replaced with the first parameter.
```

#### Controller setting
At controllet, you need add 'MessagesApi'
```
import javax.inject.Inject
import play.api.i18n.{I18nSupport, MessagesApi}

class I18nController @Inject() (val messagesApi: MessagesApi) extends Controller with I18nSupport {
```

#### use I18n
```
import play.api.i18n.Messages

need add implicit value for message :
(implicit message:Message)

Messages("info.error") == "You aren't logged in!"
Messages("example.formatting", "good man") == "When using MessageFormat, good man is replaced with the first parameter."
```
