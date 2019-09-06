### pycharm的autopep8工具的安装和使用
1. file->setting->tools->external tools，点击添加，
2. 输入下列的属性：
Name   :    autopep8
Description   :		autopep8
Program		:		autopep8
Arguments		:	--in-place --aggressive --aggressive $FilePath$
Working directory		:  	$ProjectFileDir$
Output filters		:		$FILE_PATH$\:$LINE$\:$COLUMN$\:.*
3. 然后点击cancel即可
4. 在所要规范化的代码中的右键，然后点击external tool 在点击autopep8即可，这样你的代码就符合pep8的规范啦