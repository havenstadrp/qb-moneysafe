# qb-moneysafe
Job Money Safes For QB-Core

# Adding more safes for other jobs


# This an example how you can add to the function
# function SetClosestSafe()
#    local pos = GetEntityCoords(PlayerPedId(), true)
#    local current = nil
#    local dist = nil
#    for id, house in pairs(Config.Safes) do
#        if current ~= nil then
#            if #(pos - vector3(Config.Safes[id].coords.x, Config.Safes[id].coords.y, Config.Safes[id].coords.z)) < dist then
#                current = id
#                dist = #(pos - vector3(Config.Safes[id].coords.x, Config.Safes[id].coords.y, Config.Safes[id].coords.z))
#            end
#        else
#            dist = #(pos - vector3(Config.Safes[id].coords.x, Config.Safes[id].coords.y, Config.Safes[id].coords.z))
#           current = id
#        end
#   end
#    ClosestSafe = current
#    if ClosestSafe ~= nil then
#        if current == "police" then
#            IsAuthorized = PlayerData.job.isboss
#       elseif current == "ambulance" then
#            IsAuthorized = PlayerData.job.isboss
#        end
#    end
# end

 This is how you do it in the config.lua

 NOTE that job name needs to be the name of the safe so that it knows witch job to look for.
 example:

police money safe will look for the police job and if isboss if its true then it will show him the money safe if not then player wont be able to see it.
#if current == "police" then
#IsAuthorized = PlayerData.job.isboss




# Config.Safes = {
#    ["police"] = {
#        money = 0,
#        coords = {x = 447.05, y = -974.32, z = 31.0, h = 134.5, r = 1.0},
#        transactions = {},
#    },
#    ["ambulance"] = {
#        money = 0,
#        coords = {x = 447.05, y = -974.32, z = 31.0, h = 134.5, r = 1.0}, -- You need to change the coords where you want the moneysafe to be located
#        transactions = {},
#    },
# }
