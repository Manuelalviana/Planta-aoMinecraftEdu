player.onChat("cerca", function () {
    cerca()
})
player.onChat("plantar", function () {
    for (let index = 0; index < 2; index++) {
        Fazer_rua()
        vire_a_direita()
        Fazer_rua()
        vire_a_esquerda()
    }
})
player.onChat("aqui", function () {
    agent.teleportToPlayer()
})
function Fazer_rua () {
    agent.move(UP, 1)
    for (let index = 0; index < 6; index++) {
        agent.destroy(DOWN)
        agent.till(DOWN)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.move(DOWN, 1)
}
function vire_a_esquerda () {
    agent.move(LEFT, 2)
    agent.turn(LEFT_TURN)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 1)
}
function vire_a_direita () {
    agent.move(RIGHT, 2)
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
}
player.onChat("claro", function () {
    gameplay.setWeather(CLEAR)
    gameplay.timeSet(gameplay.time(DAY))
})
function cerca () {
    agent.setSlot(2)
    agent.move(UP, 1)
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 8; index++) {
            agent.move(FORWARD, 1)
            agent.destroy(DOWN)
            agent.place(DOWN)
        }
        agent.turn(LEFT_TURN)
    }
}
