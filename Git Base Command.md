xiaoyanit.github.io
===================

My github blog .....

Git Base Command

Git ��������
com from : http://magicalboy.com/git-configuration/
1.�û���Ϣ����

	git config --global user.name "xiaoyan"
	git config --global user.email xiaoyan@gmail.com

	git config --list

2.�ı��༭��
	����Ҫ�����Ҫ���ı���Ϣʱ���ã������ύ����ʱ���˼�ע�͡�һ���������ϵͳĬ�ϵı༭��������Vi��Vim����ȻҲ�����Զ���

	$ git config --global core.editor emacs


3.�����������
	�ڽ����ͻʱ�����õ���һ��Ϊvimdiff

	$ git config --global merge.tool vimdiff

4.�Զ�����
	�����õ���ɫ��ʾ������Щ�˲�ϲ��������Ĭ���ǲ�������

	$ git config --global color.ui auto


5.�鿴����
	�鿴��������

	$ git config --list
	�鿴ĳ������

	$ git config user.name


6.git�����ļ�
	/etc/gitconfig �������û���Ч
	~/.gitconfig �Ե�ǰ�û���Ч
	{����Ŀ¼}/.git/config ���Ե�ǰ��Ŀ��Ч
	$HOME ���� C:Documents and Settings$USER �µ�.gitconfig
	git��װĿ¼�µ�/etc/gitconfig
	ͬ��
	���� unix ϵͳ�У������ļ�Ϊ��

	��Windows�ж�Ӧ�ֱ�Ϊ��

	��Ӧ���

	$ git config --system
	$ git config --global
	$ git config --local �� $ git config


7.�������������
	��ȫ���˽����������ϸ��˵��������������

	$ git help
	$ git --help
	$ man git-
	���磬Ҫѧϰ config ���������ô�ã���ִ�У�

	$ git help config







































