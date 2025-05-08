### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Добыча кварца!

## Step 1
Напиши код, который **вычислит**, сколько **блоков** тебе нужно, чтобы построить оставшиеся колонны. Вот некоторые факты: есть **6 колонн**, и каждая колонна имеет высоту **6 блоков**. Начни с создания и установки переменных ``||variable:высота||`` и ``||variable:количество||`` в правильные числа ``||loops: при старте||``, затем создай переменную ``||variable:всего блоков||``.

## Step 2
Установи условие, ``||logic: если||`` ``||variable:всего блоков||`` = ``||variable:высота||`` * ``||variable:количество||``, тогда ``||player: сказать||`` "Собрано достаточно блоков!".

## Step 3
Теперь добавь команду ``||variable:изменить всего блоков||`` на 1 и ``||player: сказать||`` ``||variable:всего блоков||``, чтобы ты знал, сколько блоков ты собрал. Убедись, что добавил ``||blocks: колонна из кварцевых блоков разрушена||``, чтобы ты видел счётчик при разрушении блоков. Когда ты закончишь, ты увидишь сообщение "Собрано достаточно блоков!".

```ghost
blocks.onBlockBroken(PILLAR_QUARTZ_BLOCK, function () {
    total_blocks += 1
    if (total_blocks == height * quantity) {
        player.say("Собрано достаточно блоков!")
    }
})
let total_blocks = 0
let quantity = 0
let height = 0
height = 6
quantity = 6
```

```template
blocks.onBlockBroken(PILLAR_QUARTZ_BLOCK, function () {
})
```