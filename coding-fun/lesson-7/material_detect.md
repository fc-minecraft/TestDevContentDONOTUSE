### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Обнаружение первого материала

## Step 1
Агенту нужно **разрушить** и затем **собрать** **золотой** блок.

```template
for (let index = 0; index < 3; index++) {
    agent.move(LEFT, 1)
    if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
        
    }
}
```

```ghost
for (let index = 0; index < 3; index++) {
    agent.move(LEFT, 1)
    if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
        agent.destroy(FORWARD)
        agent.collectAll()
    }
}
```



