##PHPWord 

- 从2003版本开始，word支持VML格式的XML文件定义word的内容
- **VML** 之**helloword**

		<?xml version="1.0"?>
		<w:wordDocument xmlns:w="http://schemas.microsoft.com/office/word/2003/wordml">
		   <w:body>
		       <w:p>
		        <w:r>
		         <w:t>Hello, World.</w:t>
		        </w:r>
		       </w:p>
		   </w:body>
		</w:wordDocument> 

- phpword 修改页边距，修改页面方向
 - phpword 计量单位 1缇=1/257cm
 
			$this->section = $this->phpWord->addSection();
	        $sectionStyle = $this->section->getSettings();
	        $sectionStyle->setMarginLeft(2154.6);
	        $sectionStyle->setMarginRight(2154.6);		//3.8cm
	        $sectionStyle->setOrientation('landscape');	//水平方向

- phpword 文本加波浪线

    	'w' => array('underline' => 'wave'),