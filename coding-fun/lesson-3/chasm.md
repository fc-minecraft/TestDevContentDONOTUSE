### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Разделенная семья!

## Step 1
Запрограммируй Агента для постройки моста через пропасть. Выдай агенту блоки.

#### ~ tutorialhint 
Требуемая длина моста - 7 блоков. Не забудь сначала выдать блоки Агенту.

```ghost
myCustomBlocks.agentSetLimitedItem(7)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)

for (let i = 0; i < 7; i++) {
    agent.move(FORWARD, 1)
    myCustomBlocks.agentPlaceBlock(DOWN)
}

``` 

```template
myCustomBlocks.agentSetLimitedItem(1)
agent.move(FORWARD, 1)
myCustomBlocks.agentPlaceBlock(DOWN)
```

```package
minecraft-hoc22=github:fc-minecraft/edu-fabric-ts#v0.0.61
```