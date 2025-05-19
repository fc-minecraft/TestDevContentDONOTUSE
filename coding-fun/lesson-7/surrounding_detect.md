### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1


### @explicitHints 1
### @flyoutOnly true

# Окружение

## Step 1
Пока Агент **осматривает блок внизу** и блок является **камнем**, Агенту нужно **двигаться вперёд**. Если Агент **не** обнаруживает блок впереди, ему также нужно двигаться вперёд, в противном случае ему нужно **повернуть налево**.

#### ~ tutorialhint
```blocks
while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
    if (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    } else {
        agent.turn(LEFT_TURN)
    }
}
```

```template
while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
    if (true) {
    } else {
    }
}
```

```ghost
while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
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
```

