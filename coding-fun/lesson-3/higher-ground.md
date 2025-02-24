### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Выше земли!

## Step 1
Запрограммируй Агента, чтобы он построил башню из **дубовых досок** высотой **10** блоков и построил лестницу высотой **10** блоков. Сначала убедись, что у Агента есть доски. Затем запрограммируй Агента, чтобы он устанавливал дубовые доски вперед, влево и вправо. После этого Агенту нужно построить лестницу.


#### ~ tutorialhint 
Используй цикл и устанавливай доски вперед, влево и вправо, поднимаясь каждый раз на один блок выше. Высота 10 блоков. Не забудь выдать блоки Агенту. 
Далее поставь лестницу так, чтобы можно было подняться, как показано на примере. Не забудь выдать лестницу Агенту.

```ghost
agent.move(FORWARD, 1)
for (let index = 0; index < 10; index++) {
myCustomBlocks.agentSetLimitedItemLadder(1)
    myCustomBlocks.agentSetLimitedItemPlanksOak(1)
    agent.move(UP, 1)
}
agent.move(DOWN, 10)
agent.turn(LEFT_TURN)

``` 
```template
myCustomBlocks.agentSetLimitedItemPlanksOak(1)
agent.move(UP, 1)
myCustomBlocks.agentPlaceBlock(FORWARD)
```



```package
minecraft-hoc22=github:fc-minecraft/edu-fabric-ts#v0.0.63
```


