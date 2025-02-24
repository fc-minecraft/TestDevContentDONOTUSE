### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Запрограммируй Агента двигаться по следам черепахи и уничтожать препятствия!

## Step 1
Запрограммируй Агента, чтобы уничтожить ствол дерева, который стоит на пути, с помощью блоков агент уничтожить и агент собрать все. Попробуй использовать блок повторить, чтобы сделать код более кратким.

```ghost
player.onChat("path", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
``` 
```template
agent.move(FORWARD, 1)
```
