-- 導入 "js" 模組
local js = require "js"
-- global 就是 javascript 的 window
local global = js.global
local document = global.document
-- html 檔案中 canvas　id 設為 "canvas"
local canvas = document:getElementById("canvas")
-- 將 ctx 設為 canvas 2d 繪圖畫布變數
local ctx = canvas:getContext("2d")

-- 屬性呼叫使用 . 而方法呼叫使用 :
-- 設定填圖顏色
ctx.fillStyle = "rgb(0,0,100)"
-- 設定畫筆顏色
ctx.strokeStyle = "rgb(0,0,200)"

-- 乘上 deg 可轉為徑度單位
deg = math.pi / 180

-- 建立多邊形定點位置畫線函式
function star(radius, xc, yc, n)
    --radius = 100
    --xc = 200
    --yc = 200
    xi = xc + radius*math.cos((360/n)*deg+180*deg)
    yi = yc - radius*math.sin((360/n)*deg+180*deg)
    ctx:beginPath()
    ctx:moveTo(xi,yi)
    for i = 2, n+1 do
        x = xc + radius*math.cos((360/n)*deg*i+180*deg)
        y = yc - radius*math.sin((360/n)*deg*i+180*deg)
        ctx:lineTo(x,y)
    end
end

-- 以下利用多邊形畫線函式呼叫執行畫框線或填入顏色
-- 畫外面六邊形框線
ctx.fillStyle= '#191980'
star(135, 202, 205, 6)
ctx:closePath()
ctx:fill()
--劃裡面白色六邊型
ctx.fillStyle = '#fff'
star(85, 200, 200, 6)
ctx:closePath()
ctx:fill()
-- 以下採用 canvas 原始座標繪圖
flag_w = 600
flag_h = 400
circle_x = flag_w/4
circle_y = flag_h/4

--上方空白
ctx.fillStyle= '#fff'
ctx:fillRect(0, 0, flag_w/2, flag_h/3)


--中間圓
ctx.fillStyle= '#191980'
star(45, 200, 200, 40)
ctx:closePath()
ctx:fill()

--中間白色
ctx.fillStyle= '#fff'
star(18, 170, 170, 4)
ctx:closePath()
ctx:fill()

--中間白色
ctx.fillStyle= '#fff'
star(18, 180, 180, 4)
ctx:closePath()
ctx:fill()
--中間白色
ctx.fillStyle= '#fff'
star(18, 190, 190, 4)
ctx:closePath()
ctx:fill()
--中間白色
ctx.fillStyle= '#fff'
star(18, 200, 200, 4)
ctx:closePath()
ctx:fill()
--中間白色
ctx.fillStyle= '#fff'
star(18, 210, 210, 4)
ctx:closePath()
ctx:fill()
--中間白色
ctx.fillStyle= '#fff'
star(18, 220, 220, 4)
ctx:closePath()
ctx:fill()

--中間白色
ctx.fillStyle= '#fff'
star(18,230, 230, 4)
ctx:closePath()
ctx:fill()

--中間白色
ctx.fillStyle= '#fff'
star(18, 240, 240, 4)
ctx:closePath()
ctx:fill()
