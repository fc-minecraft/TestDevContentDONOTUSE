### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Колонны!

## Step 1
Время строить акведуки! Сначала создай переменные ``||variable: длина||`` и ``||variable: сегменты||``. Затем ``||variable: установить длину||`` в **5** и ``||variable: установить сегменты||`` в **6** ``||loops: при старте||``.

## Step 2
Теперь внутри ``||player: по команде чата||`` тебе нужно добавить все действия, которые Агент должен выполнить, чтобы построить **1** часть: ``||agent: установить блок колонны из кварца||`` в количестве **64**, ``||agent: разместить||`` и ``||agent: двигаться вперёд||``. Вода в Minecraft будет течь, если есть уклон, поэтому Агенту нужно **разместить влево, вправо и вниз**. Помести все эти действия внутри цикла ``||loops: повторить||``, который **повторяется** ``||variable: длина||`` раз.

## Step 3
Теперь вложи первый цикл ``||loops: повторить||`` в другой цикл ``||loops: повторить||``, который повторяется ``||variables:сегменты||`` раз. 

### ~ tutorialHint
Добавь блок ``||agent: агент двигаться вниз||`` перед внутренним циклом, чтобы код работал!

```ghost
    agent.move(DOWN, 1)
    for (let index = 0; index < Segments; index++) {
        for (let index = 0; index < length; index++) {
            agent.setItem(WHITE_CONCRETE, 64, 1)
            agent.place(LEFT)
            agent.place(RIGHT)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 1)
    }
let Segments = 0
let length = 0
length = 5
Segments = 6
```
```template
agent.move(DOWN, 1)
for (let index = 0; index < 0; index++) {
    for (let index = 0; index < 0; index++) {
        agent.setItem(WHITE_CONCRETE, 64, 1)
    }
}
```