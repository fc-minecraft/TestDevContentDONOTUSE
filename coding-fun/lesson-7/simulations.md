### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Симуляция

## Step 1
Добро пожаловать в Симуляцию! Запрограммируй своего Агента, чтобы он собирал золотые блоки и уничтожал препятствия на своём пути.


```template
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
        
    }
    if (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.turn(LEFT_TURN)
    }
}

```
```ghost
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
        agent.destroy(LEFT)
        agent.collectAll()
    }
    if (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 1)
}
agent.destroy(FORWARD)
agent.collectAll()
```
