### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Спираль

## Step 1
Пока Агент **осматривает блок впереди** и блок **не** является **золотым блоком**, Агенту нужно **двигаться вперёд**. Если Агент **не** обнаруживает блок впереди, ему также нужно двигаться вперёд, в противном случае ему нужно **повернуть налево**. Когда Агент достигнет **золотого блока**, ему нужно **разрушить** и **собрать** его.

```template
while (true) {
    if (0 != 0) {
    } else {
    }
}

```
```ghost
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    } else {
        agent.turn(LEFT_TURN)
    }
}
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (agent.detect(AgentDetection.Block, FORWARD) == false) {
        agent.move(FORWARD, 1)
    } else if (agent.detect(AgentDetection.Block, FORWARD) == true) {
        agent.turn(LEFT_TURN)
    }
}
agent.destroy(FORWARD)
agent.collectAll()
```
