### @explicitHints true

### @diffs true

# Agent Reindeer

```template
player.onChat("reindeer", function () {
    riding = !(riding)
})
let riding = false
riding = false
agent.teleport(pos(0, 50, 0), NORTH)
```

## Step 1

Build this

```blocks
loops.forever(function () {
    while (riding) {
        agent.move(FORWARD, 1)
        player.teleport(positions.add(
        agent.getPosition(),
        pos(0, 0, 5)
        ))
    }
})
```

## Try it!

Type **reindeer** to go for a ride with your agent.