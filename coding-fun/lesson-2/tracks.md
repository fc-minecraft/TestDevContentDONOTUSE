### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints true


# Запрограммируй Агента двигаться вдоль тропинки черепашки!

## Step 1
Перемещай Агента вдоль тропинки черепашки к воротам, используя блок **агент: переместиться вперёд**. Когда закончишь, нажми зеленую стрелку **НАЧАТЬ**, чтобы запустить код. 

#### ~ tutorialhint 
Тебе потребуется поворачивать время от времени **агент: повернуться**.

```ghost
player.onChat("tracks", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
``` 


```template
agent.move(FORWARD, 1)
```
