### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Симуляция

## Step 1
Добро пожаловать в Симуляцию! Запрограммируй своего Агента, чтобы он собирал золотые блоки и уничтожал препятствия на своём пути.

#### ~ tutorialhint
Попробуй сначала продумать маршрут. Используй два блока **ЕСЛИ**.


```template
while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
    if (true == true) {
        
    }
    if (agent.detect(AgentDetection.Block, FORWARD)) {

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
