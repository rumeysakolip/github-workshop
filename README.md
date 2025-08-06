# Github Workshop
Github repository kullanımını daha iyi anlayabilmek, basit denemeler yapmak için bu depo oluşturdum. Üzerinde yapılabilecek bütün özelliklerini deneyerek öğreniyorum. Burada da yaptıklarımı açıklayan minik bir blok yazdım. Böylece hem ben tekrar hatırlamak istediğim bir özelliği geri dönüp inceleyebilirim, hem de yeni başlayanlar için faydalı bir kaynak olur.  

## ADIM 1 - Repository oluşturma ve commit-push işlemi  
Masaüstüne bu repository'i klonladıktan sonra vs-code üzerinden bu README.md dosyasını güncelleştirip git bash kullanarak commit ettim. Bunu yapmak için:

```bash
git clone https://github.com/rumeysakolip/github-workshop.git       # Klonla
git add README.md                                                   # Dosyayı stage et
git commit -m "README içeriği güncellendi"                          # Commit yap
```

komutlarını kullandım.  

## ADIM 2 - Yeni branch oluşturma ve pull request  
### Amaç:  
Yeni bir branch oluşturmak yeni bir deneme alanı oluşturmak için kullanılır. Orada kodlar düzgün çalışmayabilir ancak main branch her zaman doğru çalışan kodları içermelidir. Eğer bir branch'da yaptığınız değişiklikleri main branch'a eklemek istiyorsanız pull request yapabilirsiniz. Bu işlem sonrası main branch, taşıdığınız branch ile aynı olacağından bu branch'i silebilirsiniz.  

### Nasıl yaptım?  

Git bash uygulamasını çalıştırdım ve "github-workshop" repository'sinin olduğu dizine girdim. Orada yeni bir branch oluşturdum ve içerisinde bir değişiklik yapmak için txt dosyası ekledim. Değişiklikleri yeni oluşan branch'a kaydettim. Ardından GitHub repo sayfama gittim. Üstte Compare & Pull Request butonuna tıkladım. Açılan sayfada başlık ve açıklama kısımlarını doldurduktan sonra Create Pull Request’e bastım. PR (Pull Request) sayfasında Merge Pull Request butonuna bastım. Ardından Confirm Merge’e tıkladım. Bu adımlardan sonra artık değişiklikler main branch’e geçti.  

```bash
cd /c/go/to/repo/github-workshop                                        # Klasöre gitme
git checkout -b feature-branch-practice                                 # Yeni branch oluşturma
echo "Bu dosya feature branch için oluşturuldu." > branch_practice.txt  # Dosya oluşturma
git add .                                                               # Dosyayı commit’e hazırlama
git commit -m "Branch denemesi: branch_practice.txt eklendi"            # Commit atma
git push origin feature-branch-practice                                 # Branch’i GitHub’a gönderme
```
