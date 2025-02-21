### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Разделенная семья!

## Step 1
Запрограммируй Агента для постройки моста через пропасти во льду. Соедини льдины так, чтобы вме медведи оказались на центральном острове. Убедись, что у Агента в инвентаре есть блоки.

#### ~ tutorialhint 
Построй мосты любым образом, чтобы все медведи добрались до центрального острова.


```ghost
myCustomBlocks.agentSetLimitedItemPlanksOak(1)
agent.move(FORWARD, 1)
agent.place(DOWN)
agent.move(FORWARD, 1)
agent.turn(LEFT_TURN)

``` 
```template
myCustomBlocks.agentSetLimitedItemPlanksOak(1)
```



```package
minecraft-hoc22=github:fc-minecraft/edu-fabric-ts#v0.0.63
```
