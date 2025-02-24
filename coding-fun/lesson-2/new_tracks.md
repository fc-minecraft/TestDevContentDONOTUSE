### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Запрограммируй Агента двигаться вдоль тропинки черепашки!

## Step 1
Перемещай Агента вдоль тропинки черепашки, используя блок **агент: переместиться вперёд**.

#### ~ tutorialhint
Попробуй использовать блок **повторить**, чтобы сделать код более эффективным.

## Step 2
Когда закончишь, нажми на зеленую стрелку **НАЧАТЬ** чтобы запустить код.

```blocks
player.onChat("run", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
``` 

```template
agent.move(FORWARD, 1)
```

