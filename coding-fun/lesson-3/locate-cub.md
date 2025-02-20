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
for (let i = 0; i < 2; i++) {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
}
```

```ghost
agent.destroy(FORWARD)
agent.move(FORWARD, 1)
agent.destroy(UP)
for (let i = 0; i < 7; i++) {
    agent.move(FORWARD, 1)
}
``` 


```package
minecraft-hoc22=github:fc-minecraft/edu-fabric-ts#v0.0.61
```
