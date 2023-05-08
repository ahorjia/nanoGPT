
![hafezGPT](assets/hafez.jpg)

This repository is a fork of [nanoGPT](https://github.com/karpathy/nanoGPT)

It is modified (see prepare.py) to generate poetry 'similar' to Hafez.
It is trained on Hafez 500 Ghazals.

For the dependency list see the original nanoGPT project.

```
python data/hafez_char/prepare.py
```

Quick Train without GPU
```
python train.py config/train_hafez_char.py --device=cpu --compile=False --eval_iters=20 --log_interval=1 --block_size=64 --batch_size=12 --n_layer=4 --n_head=4 --n_embd=128 --max_iters=2000 --lr_decay_iters=2000 --dropout=0.0
```

```
python sample.py --out_dir=out-hafez-char --device=cpu
```

The 0.79M parameter model generates peotry such as the following, which for the given
number of parameters it is really not too bad!

```
بکنم آمد خاوهد چون چون می‌گويردم
تا کام بر و بنم دوت که باد نيست

کماد گر نمی خوش که گو در ای چنان داشت
به ميغوری بند چه لول حرد است

من عاشق گر نام در می‌رود بوی پر رفت
در به خور از رصف بر من کشت سای

که در پردان اين صگر روی جهانه
تا داردی و گويم خاک خلقايت بهشاد


غزل    ۱۲۸

خوال بر گرد حرق گيک مرغ چه گنيم و زد
بانگر که سر گفتم در گری داری

بنده به را طرب کرد کر که او جان سبرين
صد محرم به سلوين کنده‌ای تو دوش

مشا که تو از نيسته ببر اين که باش
ز دلگی به اوصوحی دل همچين دار کن


غزل    ۹۹
```
