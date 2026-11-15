\# Mening sinov kundaligim





\## 1-kun

Bugun Git va GitHub bilan ishlashni o‘rgandim.

Yangi repozitoriy yaratishni mashq qildim.



\## 2-kun

Bugun Git buyruqlarini o‘rgandim.

Fayllarni saqlashni mashq qildim.



\## 3-kun

Bugun commit nima ekanini o‘rgandim.

O‘zgarishlarni Git tarixiga saqladim.



\## 4-kun

Bugun git diff buyrug‘idan foydalandim.

Fayllardagi o‘zgarishlarni ko‘rdim.



\## 5-kun

Bugun Git bo‘yicha bilimlarimni mustahkamladim.

GitHub bilan ishlashga tayyorlandim.













Vazifalar







\## \*\*1-topshiriq. GitHub profil README\*\*



\- GitHub username: `khokimbey`

\- Repository: `khokimbey`

\- Branch: `main`

\- Yangi branch: `dizayn`

\- README fayli yaratildi.

\- Kamida 2 ta commit qilindi.

\- GitHub’ga yuklandi.



Profil havolasi: \[https://github.com/khokimbey](https://github.com/khokimbey?utm\_source=chatgpt.com)



\## \*\*2-topshiriq. Branch va Merge\*\*



\*\*1. Branch nima?\*\*



Branch — loyihaning asosiy kodiga ta'sir qilmasdan alohida ishlash imkonini beruvchi yo‘nalish.



\*\*2. Merge nima?\*\*



Merge — ikkita branch’dagi o‘zgarishlarni birlashtirish.



\*\*3. Conflict nima?\*\*



Conflict — ikkita branch’da bir xil joydagi qatorlar turlicha o‘zgartirilganda yuzaga keladigan ziddiyat.



\*\*4. Nima uchun bizda conflict chiqmadi?\*\*



Chunki `main` va `sinov` branch’lari bir xil tarixdan davom etdi. Git `Fast-forward` orqali birlashtirdi.



\*\*5. Conflict belgilarining vazifasi:\*\*



\- `<<<<<<< HEAD` — joriy branch’dagi o‘zgarish.

\- `=======` — ikki o‘zgarishni ajratuvchi belgi.

\- `>>>>>>> branch` — boshqa branch’dagi o‘zgarish.



\## \*\*Muhim Git buyruqlari\*\*



| Buyruq              | Vazifasi                      |

| ------------------- | ----------------------------- |

| `git branch`        | Branchlarni ko‘rish           |

| `git branch nom`    | Yangi branch yaratish         |

| `git switch nom`    | Branchga o‘tish               |

| `git switch -c nom` | Yangi branch yaratib o‘tish   |

| `git merge nom`     | Branchlarni birlashtirish     |

| `git branch -d nom` | Branchni o‘chirish            |

| `git merge --abort` | Merge jarayonini bekor qilish |

| `git push`          | GitHub’ga yuklash             |







3-topshiriq. Grafni o‘qish

a) 2 ta shox: main va dizayn.

b) dizayn shoxi 2d0 commit’dan keyin ajralgan. Uning commit’lari: 5b2 va 7c4.

c) Merge commit hash’i: 9a1. U main’dagi 4e8 va dizayn’dagi 7c4 commit’larini birlashtirgan.

d) Yo‘q. 4e8 main shoxida bajarilgan, dizayn shoxining alohida yo‘liga kirmaydi.

e) main’da jami 6 ta commit mavjud (1f3, 2d0, 4e8, 5b2, 7c4 va merge commit 9a1).



4-topshiriq. Conflict’ni yeching

a) HEAD — main shoxidagi «Men shifokor bo‘lmoqchiman.» varianti. «>>>>>>> tajriba» bilan tugaydigan qism — tajriba shoxidagi «Men dasturchi bo‘lmoqchiman.» varianti.

b) Faylning tozalangan holati:

\# Orzularim

Men shifokor bo‘lmoqchiman.

Men dasturchi bo‘lmoqchiman.

Sayohat qilishni yaxshi ko‘raman.

c) git add orzular.md

&#x20;  git commit



5-topshiriq. Faylda nima qoldi?

a) 3-qadamdan keyin: Salom. Chunki qizil shoxidagi o‘zgarish main’ga hali qo‘shilmagan.

b) 5-qadamdan keyin yashil shoxida: Salom va Yashil.

c) 7-qadamdan keyin main’da: Salom va Qizil. «Yashil» yo‘q, chunki yashil shoxi hali main’ga merge qilinmagan.

d) git merge yashil bajarilganda, ikkala shox ham «Salom» qatoridan keyin bir xil joyga yangi qator qo‘shganligi sababli merge conflict yuz berishi mumkin. Conflict’ni qo‘lda hal qilib, keyin add va commit bajariladi.



6-topshiriq. Xatolar va yechimlar

Git xabari	Yechim

fatal: not a git repository	B — cd bilan loyiha papkasiga kirish

! \[rejected] main -> main (fetch first)	A — git pull, keyin git push

CONFLICT (content): Merge conflict in orzular.md	D — belgilarni tozalab, add va commit

nothing to commit, working tree clean	E — hech narsa qilmaslik, hammasi saqlangan

error: pathspec 'dizayin' did not match	F — nomni git branch bilan tekshirish

Author identity unknown	C — git config --global user.name / user.email

Og‘zaki so‘rovga tayyorgarlik

•	Branch — commit’larning alohida yo‘li. Tajriba va yangi o‘zgarishlarni main’ga ta’sir qilmasdan sinash uchun alohida shox ochiladi.

•	Shox yaratish: git branch nom; shoxga o‘tish: git switch nom. Yaratish va o‘tish birga: git switch -c nom.

•	Shox almashganda Git ishchi papkadagi fayllarni tanlangan shoxdagi commit holatiga moslaydi.

•	Merge tartibi: git switch main, keyin git merge tajriba.

•	Conflict — ikki shoxda bir joy turlicha o‘zgartirilganda yuz beradi. HEAD hozirgi shox variantini, ======= chegarani, >>>>>>> qo‘shilayotgan shox variantining oxirini bildiradi. Kerakli matn qoldiriladi, belgilar o‘chiriladi, add va commit qilinadi.

•	Pull Request — GitHub’da bir shoxdagi o‘zgarishlarni ko‘rib chiqib, boshqa shoxga qo‘shishni so‘rash.

•	GitHub flow: branch → commit → push → Pull Request → merge.

•	Profil README uchun username bilan bir xil nomdagi repozitoriy yaratiladi va uning README.md fayli to‘ldiriladi.



