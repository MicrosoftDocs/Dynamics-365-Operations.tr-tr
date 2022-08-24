---
title: PDF şablonlarını doldurmak için ER yapılandırmaları tasarlama
description: Bu makalede, bir PDF şablonunu doldurmak üzere Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 4056c2b9442e26a0e1c99e6155a3cd605d222974
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283328"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>PDF şablonlarını doldurmak için ER yapılandırmaları tasarlama

[!include[banner](../includes/banner.md)]

Bu makaledeki yordamlar **Sistem Yöneticisi** veya **Elektronik raporlama geliştirici** rolündeki bir kullanıcının, rapor şablonu olarak doldurulabilir PDF belgelerini kullanarak PDF dosyaları halinde raporlar oluşturan Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini gösteren örneklerdir. Bu adımlar herhangi bir Dynamics 365 Finance şirketinde veya Regulatory Configuration Services (RCS) içinde gerçekleştirilebilir.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, bu makaledeki yordamları tamamlamak için kullandığınız hizmete bağlı olarak, aşağıdaki erişim türlerinden birine sahip olmalısınız:

- Aşağıdaki rollerden biri için Finance'a erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Aşağıdaki rollerden biri için RCS'ye erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

Ayrıca [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü de tamamlamanız gerekir.

Son olarak, aşağıdaki dosyaları indirin.

| İçerik açıklaması                       | Dosya adı                                     |
|-------------------------------------------|-----------------------------------------------|
| Raporun ilk sayfası için şablon | [IntrastatReportTemplate1. PDF](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Raporun diğer sayfaları için şablon    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Örnek ER biçimi - PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Örnek ER biçimi - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Örnek veri kümesi                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>ER biçimi yapılandırması tasarlama

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan yapılandırma listesine erişim alma

1. **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Litware, Inc.** sağlayıcısının kullanılabilir olduğundan ve etkin olarak işaretlendiğinden emin olun.
3. **Microsoft** sağlayıcısı kutucuğunda **Depolar**'ı seçin.

    > [!NOTE]
    > **LCS** türünde bir havuz zaten varsa, bu yordamın kalan adımlarını atlayın.

4. **Ekle**'yi seçin.
5. Açılan iletişim kutusunda, **Yapılandırma deposu türü** alan grubunda **LCS** seçeneğini belirleyin.
6. **Depo oluştur**'u seçin.
7. **Tamam**'ı seçin.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan model yapılandırmalarını alma

1. **Yapılandırma depoları** sayfasının sol tarafında, **Filtreleri göster** düğmesini (huni sembolü) seçin.
2. **Tür** alanında **LCS** değeri için bir filtre ekleyin ve **ile başlar** işlecini kullanın.
3. **Uygula**'yı seçin.
4. **Aç**'ı seçin.
5. Ağaçta, **Intrastat modeli** öğesini seçin.
6. **Sürümler** hızlı sekmesinde, sürüm **1**' i seçin.

    > [!NOTE]
    > **Sürümler** hızlı sekmesinde **İçe aktar** düğmesi kullanılamıyorsa, bu yordamın kalan adımlarını atlayın.

7. **İçe aktar**'ı seçin.
8. **Intrastat modeli** model yapılandırmasının seçili sürümünün içe aktarılmasını onaylamak için **Evet**'i seçin.

### <a name="create-a-new-format-configuration"></a>Yeni bir biçim yapılandırması oluşturma

1. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.
2. Ağaçta, **Intrastat modeli** öğesini seçin.
3. **Yapılandırma oluştur**'u seçin.

    > [!NOTE]
    > **Yapılandırma oluştur** düğmesi kullanılamıyorsa, **Elektronik raporlama** çalışma alanından açılabilen **Elektronik raporlama parametreleri** sayfasında tasarım modunu açmanız gerekir.

4. Açılan iletişim kutusunda **Yeni** alan grubunda, **Veri modeli Intrastatı temel alan biçim** seçeneğini seçin.
5. **Ad** alanına **Intrastat raporu (PDF)** girin.
6. **Açıklama** alanına **PDF biçiminde Intrasat raporu** yazın.

    > [!NOTE]
    > Etkin yapılandırma sağlayıcısı otomatik olarak girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilse de, yapılandırmayı sürdüremezler.

7. Isteğe bağlı: **Biçim türü** alanında, özel bir elektronik belge biçimi seçebilirsiniz. Tasarım sırasında **PDF**'yi seçerseniz, ER İşlemleri tasarımcısı yalnızca PDF formatında (**PDF\file**, **PDF\PDF Merger**, vs.) oluşturulan belgelere uygulanabilen biçim öğelerini sunacaktır. Bu alanı boş bırakırsanız, ilk biçim öğesi eklendiğinde ER İşlemleri tasarımcısında tasarım zamanında bir elektronik belge biçimi belirtilir. Örneğin, ilk biçim öğesi olarak **Excel\File**'ı eklerseniz, ER İşlemleri tasarımcısı size yalnızca Excel biçiminde oluşturulan belgelere uygulanabilen biçim öğelerini size sunacaktır (**Excel\Cell** **Excel\Range**, vb.). biçim.
8. **Yapılandırma oluştur**'u seçin.

Yeni bir ER biçimı yapılandırması oluşturulur. PDF formatında elektronik belgeler oluşturmak üzere tasarlanan ER biçim bileşenini depolamak için bu yapılandırmanın taslak sürümünü kullanabilirsiniz.

### <a name="design-the-format-of-an-electronic-document"></a>Elektronik belgenin biçimini tasarlayın.

Daha sonra, oluşturduğunuz ER biçimi yapılandırmasında **Intrastat denetim** raporunu PDF formatında oluşturan ER biçimini tasarlarsınız. Bu raporun ilk sayfası raporun özetini ve raporlanan dış ticaret hareketlerinin ayrıntılarını göstermelidir. Diğer sayfalar yalnızca, rapor edilen dış ticaret hareketlerinin ayrıntılarını göstermelidir. Oluşturulan rapor sayfalarının farklı düzenleri olması gerektiğinden, PDF biçimindeki iki farklı şablon ER biçiminde kullanılacaktır.

Herhangi bir PDF görüntüleyicisinde, indirdiğiniz PDF şablonlarını açın. Her şablonda doldurulması gereken birden çok alan bulunur. Her şablonda, dış ticaret hareketleriyle ilgili ayrıntılar, her biri dokuz alan içeren, 42 satır olarak sunulur. Satır numarası her bir alanın adının sonunda görünür (örneğin, **Tarih 1**...**Tarih 42** ve **Emtia 1**...**Emtia 42**).

Aşağıdaki resimde raporun ilk sayfası için PDF şablonu gösterilmektedir.

![Şablon 1.](media/rcs-ger-filloutpdf-template1.png)

Aşağıdaki resimde raporun diğer sayfaları için PDF şablonu gösterilmektedir.

![Şablon 2.](media/rcs-ger-filloutpdf-template2.png)

1. **Yapılandırmalar** sayfasında, **Tasarımcı**'yı seçin.
2. **Kök ekle**'yi seçin.
3. Açılan iletişim kutusunda, ağaçta **PDF \> PDF Merger**  öğesini seçin.

    **PDF Merger** öğesini biçimin kök öğesi olarak seçtiğinizde, çalışma zamanında oluşturulan tüm PDF belgeleri tek bir nihai PDF belgesinde birleştirilir. Tasarladığınız ER biçimini kullanarak gerekli tüm belgeleri oluşturmak için yalnızca bir PDF şablonuna ihtiyacınız varsa, **PDF dosyasını** kök öğe olarak seçebilirsiniz.

4. **Ad** alanına, **Çıktı** yazın.
5. **Dil tercihleri** alanında, **Kullanıcı tercihi**'ni seçin. Rapor, onu çalıştıran kullanıcının tercih ettiği dilde oluşturulacaktır.
6. **Kültür tercihleri** alanında, **Kullanıcı tercihi**'ni seçin. Raporun sayfalarında sunulan değerler ve tarihler, raporu çalıştıran kullanıcının tercih ettiği yerel ayarı temel alınarak biçimlendirilir.
7. **Tamam**'ı seçin.
8. Eylem Bölmesi'ndeki **İçe Aktar** sekmesinde, **PDF'ten aktar**'ı seçin.

    Doldurulabilir PDF belgesi bu ER biçimi için şablon olarak içe aktarıldığında, gerekli olan tüm ER biçim öğeleri (**PDF dosyası**, **Alan grubu** ve **Alan** öğeleri) otomatik olarak içe aktarılan PDf belgesinin yapısı temel alınarak tasarlanan biçimde oluşturulur.

9. **Gözat**'ı seçin. Daha önce önkoşul olarak indirdiğiniz **IntrastatReportTemplate1.pdf** dosyasına gidin ve bu dosyayı seçin.
10. **Tamam**'ı seçin.

    Seçilen dosya yüklenir ve **PDF'ten içeri aktar** iletişim kutusundaki **Şablon** alanı doldurulur.

11. **Grup alanları** seçeneğini **Evet** olarak ayarlayın. Seçili PDF belgesi herhangi bir alan grubu içeriyorsa, bunlar oluşturulan ER biçimi öğelerini gruplamak için kullanılırlar. Bu amaçla bir **Alan grubu** biçim öğesi oluşturulacaktır.

    Bu seçenek **Hayır** olarak ayarlanırsa, gerekli ER biçimi ögeleri oluşturulan **PDF Dosyası** biçimi öğesinin altında iç içe geçmiş düz bir öğe listesi olarak oluşturulur.

12. **Tamam**'ı seçin.

    ![PDF'den içe aktar iletişim kutusu.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Ağaçta, **Çıktı**'yı genişletin.

    Çalışma zamanında oluşturulan raporun ilk sayfasının oluşturulmasını yönetmek için **PDF dosyası** bileşeninin otomatik olarak oluşturulduğunu unutmayın.

14. Ağaçta, **Çıktı \> PDF Dosyası**'nı genişletin.

    Daha önce içe aktardığınız doldurulabilir PDF belgesinin yapısına bağlı olarak, bu ER biçiminde yapılandırılmış biçim öğeleri listesinin otomatik olarak oluşturulduğunu unutmayın.

15. Ağaçta, **Çıktı \> PDF Dosyası**'nı seçin.
16. **Ad** alanına, **Sayfa 1** yazın.

    Bu biçim öğesi, **Intrastat denetim** raporunun ilk sayfasını oluşturmak için kullanılır. Bu sayfa, raporun özetini ve dış ticaret hareketlerinin ayrıntılarını gösterir.

    **Dil tercihleri** alanını boş bırakırsanız, üst **PDF Merger** öğesinin **Dil tercihleri** ayarı, bu biçim öğesi kullanılarak oluşturulan raporun dilini belirler. Üst öğenin ayarını geçersiz kılmak için başka bir değer seçebilirsiniz.

    **Kültür tercihleri** alanını boş bırakırsanız, üst **PDF Merger** öğesinin **Kültür tercihleri** ayarı, bu biçim öğesi kullanılarak oluşturulan raporun yerel konumunu belirler. Yerel ayar, raporun sayfalarındaki değerlerin ve tarihlerin biçimini belirler. Üst öğenin ayarını geçersiz kılmak için başka bir değer seçebilirsiniz.

17. Eylem Bölmesinde **İçe aktar** sekmesini seçin. Seçili biçim öğesi olan **PDF Dosyası** için **PDF'ten güncelleştir** düğmesinin kullanılabilir hale geldiğini unutmayın.

    Güncelleştirilmiş PDF şablonunu düzenlenen biçime aktarmak için bu düğmeyi kullanabilirsiniz. Güncelleştirilmiş PDF şablonu içe aktarıldığında, biçim öğeleri listesi buna bağlı olarak değişecektir:

    - Güncelleştirilmiş PDF şablonundaki tüm yeni alanlar Için, düzenlenmiş ER biçiminde yeni biçim öğeleri oluşturulur.
    - Güncelleştirilmiş PDF şablonunda, düzenlenen ER biçiminde var olan herhangi bir biçim öğesine karşılık gelen alanlar artık yoksa, o biçim öğeleri ER biçiminden silinir.

18. **Biçim** sekmesinde, **Ekler**'i seçin.

    İçe aktarılan PDF belgesinin düzenlenen ER biçimine ekli olduğunu unutmayın.

    ![PDF ekini önizleme.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. İkinci PDF şablonunu içe aktararak, gerekli bağlamaları veri kaynaklarına ekleyerek bu biçimi tasarlamaya devam edin.
20. **Kaydet**'i seçin.
21. Sayfayı kapatın.
22. **Sil**'i seçin.
23. **Evet**'i seçin.

Yeni **PDF Merger**, **PDF Dosyası**, **Alan grubu** ve **Alan** biçim öğelerinin PDF formatında belge oluşturmak için nasıl kullanılabileceğini öğrenmek için örnek ER biçimini içe aktarabilir ve inceleyebilirsiniz.

### <a name="import-the-format-configuration"></a>Biçim yapılandırmasını içe aktarma

Sonra, **Intrastat denetimi** raporunu PDF formatında oluşturmak için daha önceden indirdiğiniz örnek ER biçimini içe aktarmanız gerekir. Raporun ilk sayfası raporun özetini ve raporlanan dış ticaret hareketlerinin ayrıntılarını göstermelidir. Diğer sayfalar yalnızca, rapor edilen dış ticaret hareketlerinin ayrıntılarını göstermelidir.

1. **Yapılandırmalar** sayfasında **Exchange \> XML dosyasından yükle**'yi seçin.
2. **Gözat**'ı seçin. Daha önce önkoşul olarak indirdiğiniz **Intrastat report (PDF).version.1.1.xml** dosyasına gidin ve bu dosyayı seçin.
3. **Tamam**'ı seçin.

## <a name="analyze-the-format-configuration"></a>Biçim yapılandırmasını inceleme

### <a name="format-layout"></a>Biçim düzeni

1. **Yapılandırmalar** sayfasında, ağaçta **Intrastat modeli \> Intrastat raporu (PDF)** seçeneğini belirleyin.
2. **Tasarımcı**’yı seçin.
3. **Ayrıntıları göster**'i seçin.
4. Ağaçta, **Çıktı: PDF Merger**'ı seçin.

    Bu ER biçiminin, her biri farklı PDF şablonu kullanan iki **PDF dosyası** öğesi içerdiğini unutmayın. Bir şablon, raporun ilk sayfasını PDF biçiminde oluşturmak için kullanılır ve diğer şablon diğer sayfaları oluşturmak için kullanılır.

5. Ağaçta, **Çıktı: PDF Merger \> Sayfa 1: PDF Dosyası (IntrastatReportTemplate1)** öğesini genişletin.
6. Ağaçta, **Çıktı: PDF Merger \> Sayfa N: PDF Dosyası (IntrastatReportTemplate2)** öğesini genişletin.

    İki PDF şablonunun içeriği farklı olduğundan, iki **PDF Dosyası** öğesi için iç içe geçmiş biçim öğelerinin yapısının farklı olduğunu unutmayın.

### <a name="format-mapping"></a>Biçim eşleme

1. **Biçim tasarımcısı** sayfasında **Eşleme** sekmesini seçin.
2. Ağaçta **Kapsamlı arama \> Sayfalar**'ı genişletin.

    ![Model ağacının genişletilmiş olduğu formül tasarımcısı sayfası.](media/rcs-ger-filloutpdf-reviewformat.png)

    Aaşağıdaki ayrıntıları unutmayın:

    - **PDF Dosyası** türünün **Çıktı \> Sayfa 1** biçim öğesi herhangi bir veri kaynağıyla ilişkili değildir ve bu biçim öğesinin **Etkin** ifadesi boştur. Bu nedenle, çalışma zamanında **IntrastatReportTemplate1** PDF şablonu ayrı bir PDF belgesi oluşturulduğunda yalnızca bir kez doldurulacaktır.
    - **PDF Dosyası** türünün **Çıktı \> Sayfa N** biçim öğesi **Kayıt listesi** türünün **Paging.PageN** veri kaynağına bağlıdır ve bu biçim öğesinin **Etkin** ifadesi boştur. Bu nedenle, çalışma zamanında **IntrastatReportTemplate2** PDF şablonu ayrı bir PDF belgesi oluşturulduğunda bağlı kayıt listesindeki her kayıt için doldurulacaktır.
    - **Sayfa 1: PDF Dosyası** ve **Sayfa N: PDF Dosyası** biçim öğeleri **Çıktı: PDF Merger** biçim öğesinin alt öğeleri olduğundan doldurulan tüm PDF belgeleri tek bir PDF dosyasında birleştirilecektir.
    - **Paging.Page1** ve **Paging.PageN** veri kaynakları **Paging.Pages** veri kaynağıdan kayıt filtreleri olarak yapılandırılır. Bu veri kaynağı tüm dış ticaret hareketleri kümesini toplu işlemlere bölmek için yapılandırılır. Her toplu iş en çok 42 kayıt içerir. Aşağıdaki ER ifadesi, hareketleri toplu işlemlere bölmek için kullanılır:

        SPLITLIST(Totals.CommodityRecord,42)

    - **Paging.Pages** veri kaynağı, **Paging.Pages.Enumerated** öğesini içerir ve bir toplu işte bulunan her kaydın ayrıntılarını döndürür. Bu ayrıntılar, kaydın geçerli toplu işteki sırasını içerir (**Paging.Pages.Enumerated.Number** alanı). **Paging.Pages.Enumerated.Number** alanı **PDF Alanı** biçim öğelerinin **Ad** ifadesinde toplu işteki hareket numarasını temel alarak dinamik olarak bir alan adı oluşturmak için kullanılır. Oluşturulan alan adı daha sonra kullanılan PDF şablonunun doğru PDF alanını doldurmak için kullanılır.
    - **PDF Grubu** türünün **Çıktı \> Sayfa N \> Ayrıntılar 2** biçim öğesi **Kayıt listesi** türünün **Paging.PageN.Enumerated** veri kaynağıma bağlıdır (veya **Göreli yol** görüntüleme modu kullanılırsa **\@.Enumerated**). Bu nedenle, çalışma zamanında, bu PDF grubunun iç içe yerleştirilmiş öğeleri, bağlı kayıt listesindeki her kayıt için doldurulacaktır. Bu şekilde, her bir PDF satırı **Paging.PageN.Enumerated** listesinin 42 kaydının her N'inci kaydı için sanal olarak oluşturulur, şu PDF alanları doldurulur: Tarih N, Yön N, Emtia N, vb. Bu nedenle, **Alan grubu** biçim öğesinin davranışı **XML \> Sıra** ve **Metin \> Sıra** biçim öğelerinin davranışına benzer.

3. Ağaçta **Çıktı \> Sayfa N \>Details2** öğesini genişletin.
4. Ağaçta **Çıktı \> Sayfa N \> Details2 \> PageFooter** öğesini seçin.

    Bu biçim öğesinin **Ad** özniteliðinin **PageFooter** olarak tanımlandığına dikkat edin. Ayrıca, biçim öğesinin **Ad** ifadesinin boş olduğuna da dikkat edin.

5. Ağaçta **Çıktı \> Sayfa N \> Details2 \> Correction 1** öğesini seçin.

    Bu biçim öğesinin **Ad** özniteliğinin **Correction 1** olarak tanımlandığına dikkat edin. Ayrıca, biçim öğesinin **Ad** ifadesinin **Paging.FldName("Correction",\@.Number)** olarak tanımlandığına dikkat edin.

![Bir eşlemenin seçildiği biçim tasarımcısı.](media/rcs-ger-filloutpdf-reviewformat2.png)

**Alan** biçimi öğesinin, üst **PDF dosyası** biçim öğesinin şablonu olarak tanımlanan, doldurulabilir bir PDF belgesinin tek bir alanını doldurmak için kullanıldığını unutmayın. **PDF dosyası** biçim öğesi veya iç içe yerleştirilmiş öğelerinin bağlaması, iç içe yerleştirilmiş öğeleri varsa, ilgili PDF alanlarına girilen değeri belirtir. **Alan** biçim öğesinin farklı özellikleri, hangi PDF alanının tek bir biçim öğesi tarafından doldurulacağını belirtmek için kullanılabilir:

- **Biçim** sekmesinde, biçim öğesinin **Ad** özniteliği
- **Eşleme** sekmesinde, biçim öğesinin **Ad** ifadesi

Bir **Alan** biçimi öğesi için her iki özellik de isteğe bağlı olduğundan, hedef PDF alanını belirtmek için aşağıdaki kurallar uygulanır:

- **Ad** özniteliği boşsa ve çalışma zamanında **Ad** ifadesi boş bir dize döndürürse, kullanıcıya PDF belgesini doldurmak için kullanılan PDF şablonunda bir PDF alanının bulunamadığını bildirmek amacıyla çalışma zamanında özel durum oluşturulur.
- **Ad** özniteliği tanımlanmışsa ve **Ad** ifadesi boşsa, biçim öğesinin **Ad** özniteliğiyle aynı ada sahip PDF alanı doldurulur.
- **Ad** özniteliği tanımlanmışsa ve **Ad** ifadesi yapılandırılmışsa, biçim öğesinin **Ad** ifadesi tarafından döndürülen değerle aynı ada sahip PDF alanı doldurulur.

> [!NOTE]
> PDF şablonundaki bir onay kutusu, bir onay kutusu grubuna ait olmadığında, **PDF dosya** öğesinin altında yuvalanmış bir **Alan** öğesi olarak düzenlenebilir bir ER biçiminde temsil edilir. Bu PDF onay kutusu türü, aşağıdaki yollarla seçili şekilde doldurulabilir:
>
> - Karşılık gelen **Alan** biçimi öğesi, **Doğru** değeri olan *[Boolean](er-formula-supported-data-types-primitive.md#boolean)* veri türünün veri kaynağı alanına bağlanır.
> - Karşılık gelen **Alan** biçimi öğesi, metin değeri **1**, **Doğru** veya **Evet** olan bir veri kaynağı alanına bağlı iç içe geçmiş **Dize** biçimi öğesi içerir.
>
> Şablonunuz, bir seferde yalnızca bir onay kutusunun seçilebileceği bir grup onay kutusu içerebilir. Bu onay kutuları bir PDF şablonunda, *ONAY KUTUSU* türünde birden çok form alanı olarak gösterilir. Her alan aynı ada ancak farklı dışa aktarma değerine sahiptir. Şablonu düzenlenebilir ER biçimine içe aktardığınızda, her onay kutusu aynı **Onay kutusu grubu maddesi** altında yuvalanmış bir **Onay kutusu grup maddesi** olarak biçim hiyerarşik yapısında temsil edilir. **Onay kutusu grubu** öğesinin adı, PDF şablonundaki onay kutusu alanları adına eşit olacak. Her bir **Onay kutusu grubu maddesi** öğesinin adı, PDF şablonundaki karşılık gelen onay kutusu alanının dışa aktarma değerine eşit olacak.
>
> **Onay kutusu grubu maddesi** öğesini yalnızca *Boole* veri türündeki veri kaynağı alanına bağlayabilirsiniz.

## <a name="run-the-format-configuration"></a>ER biçimi yapılandırması çalıştırma

### <a name="import-the-format-configuration"></a>Biçim yapılandırmasını içe aktarma

Sonra, **Intrastat (Excel 'den içe aktar)** örnek ER biçimini yüklersiniz. Bu biçim, kullanıcının seçtiği dış ticaret hareketlerine benzetim yapan bir Microsoft Excel çalışma kitabını ayrıştırmaya yönelik tasarlanmıştır.

1. **Yapılandırmalar** sayfasında **Exchange \> XML dosyasından yükle**'yi seçin.
2. **Gözat**'ı seçin. Daha önce önkoşul olarak indirdiğiniz **Intrastat (import from Excel).version.1.1.xml** dosyasına gidin ve bu dosyayı seçin.
3. **Tamam**'ı seçin.
4. Ağaçta, **Intrastat (model) \> Intrastat (import from Excel)** öğesini seçin.
5. **Düzenle** öğesini seçin.
6. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > **Intrastat modeli** yapılandırması için  veya **Intrastat modeli** yapılandırması altında iç içe yerleşmiş olan başka bir yapılandırma için **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarladıysanız bu seçeneği **Hayır** olarak ayarlayın. 

    **Model eşleme için varsayılan** seçeneği **Evet** olarak ayarlandığında, içe aktarılan **Intrastat (Excel'den içe aktar)** ER biçimi, **Intrastat raporu (PDF)** biçimi yapılandırması için varsayılan veri kaynağı olarak atanır. Daha sonra, **Intrastat raporu (PDF)** biçimi yapılandırması çalıştırıldığında, **Intrastat (Excel'den içe aktar)** ER biçimi tarafından ayrıştırılan Excel çalışma kitabının içeriği bildirilmesi gereken dış ticaret hareketlerinin benzetimini yapar. Aşağıdaki şekilde bir Excel çalışma kitabı örneği gösterilmiştir.

    ![Örnek verileri olan Excel çalışma kitabı.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>ER biçimi yapılandırması çalıştırma

1. **Yapılandırmalar** sayfasında, ağaçta **Intrastat modeli \> Intrastat raporu (PDF)** seçeneğini belirleyin.
2. **Çalıştır**'ı seçin.
3. **Gözat**'ı seçin. Daha önce önkoşul olarak indirdiğiniz **Intrastat sample data.xlsx** dosyasına gidin ve bu dosyayı seçin.
4. **Tamam**'ı seçin.
5. **Rapor yönü** alanında, oluşturulan PDF raporunda içe aktarılan Excel çalışma kitabından gelen tüm hareketleri doldurmak için **Her ikisi** seçeneğini seçin.
6. **Tamam**'ı seçin.
7. Oluşturulan PDF belgesini gözden geçirin.

Takip eden resim, oluşturulan raporun ilk sayfasının bir örneğini gösterir.

![Oluşturulan raporun ilk sayfası.](media/rcs-ger-filloutpdf-generatedreport.png)

Takip eden resim, oluşturulan raporun diğer sayfasının bir örneğini gösterir.

![Oluşturulan raporun diğer sayfası.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Sınırlamalar

Doldurulabilir alanların adları, rapor şablonu olarak kullanmayı planladığınız PDF formunda benzersiz olmalıdır. Her bu tür alan için, bir PDF formu içe aktarıldığında, ilgili ada sahip bağımsız bir biçim öğesi düzenlenebilir bir biçimde oluşturulur. Bir PDF formu aynı adda birden fazla alan içeriyorsa, alanlar için çalışma süresinde her zaman ayrı olarak doldurulmalarına izin vermeyen tek bir biçim öğesi oluşturulur.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>PDF biçiminde bir rapor oluşturmak için ER biçimini kullandığımda, neden aşağıdaki hataları alıyorum: **İref akışları işlenemiyor. PDFSharp'ın geçerli uygulaması Acrobat 6 ile tanıtılan bu PDF özelliğini işleyemez.** ve **PDF adı eğik çizgiyle (/) başlamalıdır.**

ER çerçevesi, bu PDF raporlarını oluşturmak için PDFSharp kitaplığı sürüm 1.5 kullanır. PDF 1.5'in ( Adobe Reader 6.0) bazı özellikleri henüz bu kitaplığa uygulanmıyor. Bu nedenle, PDFSharp **PDF 1.5 veya üzeri** olarak işaretlenmiş bazı dosyaları açamıyor ve alınan hatalara neden olabilir. Sorunu çözmek için aşağıdaki çözümlerden birini kullanın:

-   Kendi PDF şablonunuzu kullandığınızda: şablonu önceki bir Adobe sürümüne indirgeme ve bu biçimde yeni bir şablon kullanmaya başlama.
-   ER çözümünün bir parçası olarak başka bir konfigürasyon sağlayıcısı tarafından sizinle paylaşılan bir ER form biçimi şablonu kullandığınızda: Bu ER çözümünün sahibine başvurun ve soruna ilişkin bir açıklama verin.
-   PDFSharp kitaplığının önceki bir sürümünü içeren ISV çözümünü kullandığınızda: Çözümün sahibine başvurun ve daha yeni PDFSharp sürümüne yükseltme önerin.

## <a name="additional-resources"></a>Ek kaynaklar

- [ER OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama (Kasım 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Word biçiminde raporlar oluşturmak için ER yapılandırmaları tasarlama](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
