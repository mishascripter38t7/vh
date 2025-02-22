local functions = {}

-- Функции команд
function functions:SetAdmin()
    print("Вы стали админом!")
end

function functions:GiveImmortality(player)
    -- Пример включения бесмертия для игрока
    print(player .. " теперь бессмертный!")
end

function functions:Fly(player)
    -- Пример активации полета для игрока
    print(player .. " теперь может летать!")
end

function functions:Chaos()
    print("Режим хаоса включен!")
    -- Можете добавить хаос с рандомными эффектами
end

function functions:AntiCheat()
    print("Анти-чит система активирована!")
end

function functions:KickPlayer(player)
    print(player .. " был кикнут!")
end

function functions:BanPlayer(player)
    print(player .. " был забанен!")
end

function functions:Invisible(player)
    print(player .. " стал невидимым!")
end

function functions:KillAllPlayers()
    print("Убийство всех игроков произошло!")
    -- Код для убийства всех игроков
end

function functions:FreezePlayer(player)
    print(player .. " заморожен!")
    -- Код для заморозки игрока (невозможность двигаться)
end

function functions:TeleportPlayer(player, location)
    print(player .. " телепортирован в " .. location)
    -- Код для телепортации игрока в указанное место
end

function functions:GiveWeapon(player, weapon)
    print(player .. " получил оружие: " .. weapon)
    -- Код для выдачи оружия игроку
end

function functions:CreateExplosion()
    print("Взорвана большая бомба!")
    -- Код для создания взрыва
end

function functions:SendMessage(message)
    print("Сообщение: " .. message)
    -- Отправить сообщение всем игрокам
end

function functions:DestroyBuilding(building)
    print(building .. " уничтожено!")
    -- Уничтожить здание или объект
end

function functions:SpawnVehicle(vehicle)
    print("Спавн транспортного средства: " .. vehicle)
    -- Спавн указанного транспортного средства
end

function functions:ActivateSuperSpeed(player)
    print(player .. " теперь может бегать с суперскоростью!")
    -- Код для включения суперскорости игрока
end

function functions:GiveSuperJump(player)
    print(player .. " теперь может прыгать очень высоко!")
    -- Код для включения суперпрыжка
end

function functions:SummonMonster()
    print("Монстр был призван!")
    -- Призвать монстра или NPC
end

function functions:ActivateNightMode()
    print("Ночной режим активирован!")
    -- Включить ночной режим
end

function functions:DisableGravity()
    print("Гравитация отключена!")
    -- Отключить гравитацию на сервере
end

-- Обработка команд
function ExecuteCommand(command, player, argument)
    if functions[command] then
        if argument then
            functions[command](argument)
        else
            functions[command]()
        end
    else
        print("Команда не найдена!")
    end
end

-- Пример использования
ExecuteCommand("SetAdmin")             -- Стать админом
ExecuteCommand("GiveImmortality", "Player1")  -- Дать бесмертие
ExecuteCommand("Fly", "Player1")      -- Включить полет для игрока
ExecuteCommand("KillAllPlayers")      -- Убить всех игроков
