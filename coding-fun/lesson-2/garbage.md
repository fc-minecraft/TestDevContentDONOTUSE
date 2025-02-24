### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Запрограммируй Агента собрать весь мусор!

## Step 1
Запрограммируй Агента, чтобы очистить тропинку черепашки, с помощью блоков **агент: уничтожить** и **агент: собрать все**. Попробуй использовать блок **повторить**, чтобы сделать код более кратким.


```ghost
player.onChat("garbage", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
```template
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 1)
}
```
