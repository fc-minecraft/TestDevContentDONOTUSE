### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Найди выход!

## Step 1
Запрограммируй расчистку пути Агентом. Глубина завала - 9 блоков.

#### ~ tutorialhint 
Нужно выкопать путь высотой 2 блока и длиной 9 блоков.

```template
agent.move(FORWARD, 1)
agent.destroy(FORWARD)
```

```ghost
agent.destroy(FORWARD)
agent.move(FORWARD, 1)
agent.destroy(UP)
``` 


```package
minecraft-hoc22=github:fc-minecraft/edu-fabric-ts#v0.0.61
```
