-- Blade Ball Auto Parry Script

-- Konstanten
local player = game.Players.LocalPlayer
local bladeBall = workspace.BladeBall -- Stelle sicher, dass dies der richtige Name des Objekts in deinem Spiel ist

-- Funktion zum automatischen Parieren
local function autoParry()
    while true do
        wait() -- Warte eine kurze Zeitspanne zwischen den Aktionen
        
        -- Überprüfe, ob der Blade Ball existiert und in Reichweite ist
        if bladeBall and (player.Character.HumanoidRootPart.Position - bladeBall.Position).magnitude <= 10 then
            -- Parieren, indem die linke Maustaste gedrückt wird
            mouse1click()
        end
    end
end

-- Starte die Auto Parry Funktion im Hintergrund
spawn(autoParry)

