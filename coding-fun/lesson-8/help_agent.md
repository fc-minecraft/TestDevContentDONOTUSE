### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Железо

## Step 1
Пока Агент **осматривает блок внизу** и этот блок **не** является **железной рудой**, ему нужно **двигаться вперёд**. Если Агент **обнаруживает блок впереди**, то ему нужно **разрушить его**. Когда Агент находит железо, запрограммируй его, чтобы он **собрал** его. Обрати внимание, что для того, чтобы собрать блок, Агенту нужно сначала его разрушить.

```template
agent.move(FORWARD, 1)
```

```ghost
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the iron ore!")
    agent.destroy(DOWN)
    agent.collectAll()
```
