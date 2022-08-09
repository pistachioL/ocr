# 图片二值化
from PIL import Image
import pytesseract
img = Image.open('test.png')

Img = img.convert('L')
Img.save("test1.jpg")

threshold = 200

table = []
for i in range(256):
    if i < threshold:
        table.append(0)
    else:
        table.append(1)

# 图片二值化
photo = Img.point(table, '1')
photo.save("test2.jpg")


code = pytesseract.image_to_string(photo, lang='chi_sim')
print(code)
