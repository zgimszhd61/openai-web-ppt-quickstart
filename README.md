# openai-web-ppt-quickstart


```
!pip install python-pptx

from pptx import Presentation
from pptx.util import Inches

# 创建一个演示文稿对象
prs = Presentation()

# 添加第一个幻灯片
slide1 = prs.slides.add_slide(prs.slide_layouts[1])  # 使用第二种布局
title1 = slide1.shapes.title
subtitle1 = slide1.placeholders[1]
title1.text = "欢迎来到我的演示文稿"
subtitle1.text = "这是使用python-pptx创建的"

# 添加第二个幻灯片
slide2 = prs.slides.add_slide(prs.slide_layouts[5])  # 使用空白布局
txBox = slide2.shapes.add_textbox(Inches(2), Inches(2), Inches(4), Inches(1.5))
tf = txBox.text_frame
tf.text = "这是第二个幻灯片"

p = tf.add_paragraph()
p.text = "这里是第二个段落的内容"

# 保存演示文稿
prs.save('demo_presentation.pptx')
```

