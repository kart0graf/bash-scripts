# bash-scripts
## Введение
Выкладываю полезные скрипты на bash с кратким описанием их работы.
Заранее благодарю всех, кто советами, идеями и кодом помогал в создании скриптов.
## Информация об окружении в котором выполняются скрипты.
На рабочих и домашних компах установлены xubuntu 18.04, debian 9. 
Для выполнения скриптов предпочитаю bash. 
Если будут использоваться какие то специфические программы я их укажу.
## Скрипты для работы с изображениями.
Скрипты для задач конвертацией множества растровых файлов из формата в формат, всевозможные bmp, jpg, djvu, pdf, png. Для конвертации обычно нужен ImageMagick. 
Скрипты по работе с геопривязанными растрами, будут лежать отдельно.

### [BMPtoJPG](https://github.com/kart0graf/bash-scripts/blob/master/work_with_images/BMPtoJPG)
Создает папку JPG в текущей, туда попадают конвертированные из BMP в jpg  файлы. Файлы перебираются  из текущей папки. Могут быть проблемы с пробелами в названиях файлов.

### [jpg2000px](https://github.com/kart0graf/bash-scripts/blob/master/work_with_images/jpg2000px)
Похож на предыдущий скрипт. Создает папку **small** в текущей. Перебирает файлы в формате jpg и уменьшает их до размера в 2000px с качеством 90. 

### [PNGtoJPG](https://github.com/kart0graf/bash-scripts/blob/master/work_with_images/PNGtoJPG)
Подобен **BMPtoJPG**. 

### [convertBMPtoJPG.bat](https://github.com/kart0graf/bash-scripts/blob/master/work_with_images/convertBMPtoJPG.bat)
Этот скрипт сделан для Windows. Тоже требуется установленный imageMagick.
Он ищет файлы bmp в текущей папке и в подпапках, и конвертирует их в jpg. Исходные файлы не удаляются. 

### [optimizeJPGandPNG](https://github.com/kart0graf/bash-scripts/blob/master/work_with_images/optimizeJPGandPNG)

Скрипт посложнее. Служит для оптимизации изображений в формате **jpg** и **png**. Например для размещения на сайте. Кроме **ImageMagick** требуются еще установленные **jpegoptim** и **optipng**. А также **rsync**. 

В файле скрипта можно задать переменные с максимальным размером картинки и качеством сжатия для  **jpg**.

Каталог с картинками должен называться **all**, кладется в текущий. В нем могут быть и другие файлы.

Скрипт создает каталог **output**. Копирует в него файлы форматов **jpg** и **png**, по возможности сохраняет структуру каталогов и права.

Меняет размер файлов, если он больше 1600px. 

Затем оптимизирует файлы для веб.

Доплнительно делаются файлы с отчетам, логом, ошибками.

Комментарии кода есть в самом скрипте.










