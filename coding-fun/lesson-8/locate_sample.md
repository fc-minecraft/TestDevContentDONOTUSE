### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1
### @flyoutOnly true

# Найди образец!

## Step 1
**Пока** Агент **осматривает блок внизу** и **не** находит **голубого льда**, запрограммируй Агента, чтобы он **разрушал** и **двигался вниз**. Когда Агент находит **голубой лёд**, ему нужно **разрушить внизу** и **собрать** образец.


```template
agent.move(FORWARD, 1)
```

```ghost 
while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
    agent.destroy(DOWN)
    agent.move(DOWN, 1)
}
agent.destroy(DOWN)
agent.collectAll()
```

