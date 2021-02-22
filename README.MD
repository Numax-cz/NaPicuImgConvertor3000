# NapicuConvertor3000
* Není potřeba instalovat balíčky
* Použitý balíček - Pillow 8.1.0
# Nastavení 
* Program vezme všechny png soubory ve vašem adresáři a convertuje je na webp
* Program sám nemaže staré obrázky
```python
from PIL import Image  
import glob
for file in glob.glob("*.png"): #Zde si nastavíte přijímací formát 
    #Tato funkce vezme všechny png soubory ve vašem adresáři 
    img = Image.open(file)
    rgb_im = img.convert('RGBA') #RGB jestli chete pozadí
    rgb_im.save(file.replace("png", "webp"), quality=100) 
                #(file.replace(z formátu, na formát), kvalita=Hodnota kvality)
```