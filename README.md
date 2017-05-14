# zinnia-blog
my-blog

建议使用python虚拟环境
python3.5中的虚拟环境设置方式
python -m venv .
linux中执行这个使虚拟环境生效
source bin/active

安装参考
http://docs.django-blog-zinnia.com/en/develop/getting-started/install.html

其他
修改blog.setting.py
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR, 'templates')],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

增加markdown支持
ZINNIA_MARKUP_LANGUAGE = 'markdown'
ZINNIA_MARKDOWN_EXTENSIONS = ['markdown.extensions.extra', 'markdown.extensions.codehilite']

复制模板文件到项目，Lib\site-packages\zinnia\templates\zinnia复制到和mange.py同级的templates目录

python manage.py migrate

python manage.py createsuperuser

python mange.y runserver
