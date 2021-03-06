<h1 align="center"> Koply Core Async Bot Base </h1>

[![Build Status](https://travis-ci.com/musabrt/koply-core.svg?branch=master)](https://travis-ci.com/musabrt/koply-core)
![LICENSE](https://img.shields.io/github/license/MusaBrt/koply-core?style=flat)
![stars](https://img.shields.io/github/stars/MusaBrt/koply-core?style=flat)

Simple bot base includes CommandHandler and Config system.

## How To Create A Command
```java
@CommandName("ping")
@CommandDescription("Pong!")
public class PingCommand extends Command {

    @Override
    public void handle(CommandParameters cmd) {
        cmd.getTextChannel().sendMessage("Pong!").queue();
    }
}
```
_Optionally you can use final class and final handle method. This will be nicer._

`@CommandName`: Command's name for usage. 

`@CommandDescription`: Command's description for help command.

`@OwnerOnly`: This command usable for only bot owners.

## Config.json Syntax

`"prefix": "$"`: For command prefix.

`"token": "INSERT-BOT-TOKEN-HERE"`: Bot token.

`"owners": ["INSERT-YOUR-ID-HERE"]`: Bot owner id's.

`"cooldown": 5000`: Cooldown for regular users. The bot owners are doesn't affect the cooldown.

### Group Names And Descriptions

`"info": "Bilgilendirme--Bilgi alabileceğiniz komutlar bulunur."`: The key named as 'info' for 'info' commands package. The group name is before then '--'. The group description is after then '--'.

`"nulldescriptiontext": "Açıklama girilmedi."`: This line for non-descriptioned commands.

## Versions Changelog

<details>
  <summary>v2.0</summary>
    <p> * Added file database (json) system.<br>
        * Fixing some bugs.</p>
</details>




