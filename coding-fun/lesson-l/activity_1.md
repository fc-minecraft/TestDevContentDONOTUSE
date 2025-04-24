### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Лабиринт

## Правило левой руки
Чтобы найти выход из лабиринта, ты можешь использовать правило левой руки. Вот как это работает:

1. Смотри, что находится слева от тебя. Если там нет стены, то поверни налево и иди вперед.

2. Если слева есть стена, но впереди нет, то просто иди вперед.

3. Если и слева, и впереди есть стены, то поверни направо.


```template
//
``` 

```ghost
while (agent.inspect(AgentInspection.Block, DOWN) != GOLD_BLOCK) {
    if (!(agent.detect(AgentDetection.Block, LEFT))) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
    } else if (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    } else {
        agent.turn(RIGHT_TURN)
    }
}
if (agent.detect(AgentDetection.Block, FORWARD) == false) {
    agent.move(FORWARD, 1)
}
``` 
