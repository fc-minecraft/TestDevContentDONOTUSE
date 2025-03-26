### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Добраться до магмы

## Step 1
Запрограммируй Агента, чтобы он **двигался вперёд**. Пока Агент **осматривает** блок **внизу** и это **не магма**, Агенту нужно **двигаться вниз**.

```template
agent.move(FORWARD, 1)
```

```ghost
agent.move(FORWARD, 1)
while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
    agent.move(DOWN, 1)
}
```

