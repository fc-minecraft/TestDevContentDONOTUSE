### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# 3D Пространство

## Step 1
Чтобы решить этот вызов, тебе нужно запрограммировать Агента, чтобы он добрался до **золотого** блока и собрал его. Агенту нужно сначала сделать это на уровне земли, а затем **подняться на 3 уровня вверх** и повторить все действия.


```template
for (let index = 0; index < 2; index++) {  
    while (true) {
    }
}
``` 
```ghost
for (let index = 0; index < 2; index++) {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
    agent.move(UP, 3)
}
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (agent.detect(AgentDetection.Block, FORWARD) == false) {
        agent.move(FORWARD, 1)
    } else if (agent.detect(AgentDetection.Block, FORWARD) == true) {
        agent.turn(LEFT_TURN)
    }
}
```