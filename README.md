# video_music_book_datasets
NLP NER datasets video/music/book bio


# 介绍
类似于人名/地名/组织机构名的命名体识别数据集,我花了几天时间标注了大约10000条视频/音乐/书籍数据.

数据的意义希冀能够基于此训练NLP模型识别句子中的视频/音乐/书籍等名称信息.

数据的标注过程:
+ 先纯手动提取标记了一部分(大约5000条),基于标注数据训练一个base模型,基于base模型重新审视校正标注数据.
+ 基于校正后的数据再训练一个模型,基于模型标注了另外约5000条数据.并对数据进行人工审核校验.
+ 最终数据集包含9632条数据.


理论上来说,任务也会是标准的NER任务.
难点:同一个名称可能是书籍也可能是视频(电视电影可能是由小说改编而来,有些场景关注书籍,另外一些可能关注视频),有些句子则只是提供了一长串并列的名称,可能没有更多的辅助信息;


示例:
``` text
放暑假了，最近剧荒，陈情令也才一个星期更新三次，根本不够看，问问大家有什么好看的电视剧或电影推荐吗？最好是那种搞笑，温暖的那种，日剧也可以，好像道骏枝佑的剧还不错！
label: 陈情令/video

最近有没有好看的电视剧推荐，国内国外的都可以，前两天再追少年派，但剧情走向越来越扯，非常想给编剧寄刀片，现在想看些正常三观的剧，大家有没有推荐哒？
label: 少年派/video

最近有些剧荒啊，有什么好看的电视剧或者电影可以推荐么？我看的也比较杂，权力的游戏，黑色止血钳，最近看的韩剧囚犯医生是大爱啊，类似这种类型的可以给我推荐一些么？
label: 权力的游戏/video	黑色止血钳/video	囚犯医生/video

我个人比较喜欢听古风歌曲，然后呢，我歌单里面可以给你推荐几首，归去来兮琵琶行清明上河图好可以去试着搜索一些古装剧的主题曲或者插曲
label: 归去来兮/music	琵琶行/music	清明上河图好/music

不知道你喜欢什么类型的小说，最近在看十宗罪，悬疑烧脑类的，讲述的是公安部门打击违法犯罪的故事，现在已经出到第六部了，估计够你看一个月了。大冰写的书也可以尝试看一下，文艺小清新类型的
label: 十宗罪/book
```

最终提供的数据集转换成了标准的BIO标注格式,欢迎尝试使用.



# Copyrights & Cite
LG: ourantech@163.com

Blog: https://www.ourantech.club/2019/08/31/029_视频音乐书籍标注数据/

Github: https://github.com/LG-1/video_music_book_datasets
