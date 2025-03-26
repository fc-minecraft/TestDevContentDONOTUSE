### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Окружение

## Step 1
Пока Агент **обнаруживает блок внизу**, ему нужно двигаться вперёд. Если Агент **осматривает блок внизу** и находит **воздух**, используй команду **сказать**, чтобы сказать **Кратер найден!**



```template
            player.say("")
```
```ghost
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("Кратер найден!")
    }
```