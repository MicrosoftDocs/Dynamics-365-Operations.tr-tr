---
title: Sosyal Hak yönetiminde Ekonomik Bakım Yasası raporları oluşturma
description: Bu makalede, Kazanç yönetiminin Ekonomik Bakım Yasası (ACA) işveren yönergesine yönelik olarak Form 1095-B ve Form 1095-C'de bildirilen bilgileri nasıl izlediği açıklanmaktadır.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a56fe2b3a25a300687d81702c52614a78f2a6f61
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337082"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Sosyal Haklar yönetiminde ACA raporları oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kazanç yönetimi, Ekonomik Bakım Yasası (ACA) işveren yönergesi için Form 1095-B ve Form 1095-C'de bildirilen bilgileri izler. Eski **Sosyal Haklar** çalışma alanında ACA raporlama özelliği gibi, bu işlevsellik yalnızca ABD'deki tüzel kişilikler için geçerlidir.

Bu işlevi kullanmak için, önce **Gelişmiş Sosyal Haklar Yönetimi**'ni açmalısınız. Sosyal Haklar yönetimi hakkında önemli uyarılar da dahil olmak üzere daha fazla bilgi için, bkz. [Sosyal Haklar yönetimini etkinleştirme veya devre dışı bırakma](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> ACA raporlamasını yalnızca **Sosyal Haklar yönetimi** çalışma alanından veya eski **Sosyal Haklar** çalışma alanından (her ikisinden değil) kullanabilirsiniz. Örneğin, Sosyal Haklar yönetimine geçtiyseniz, ACA raporlaması eski **Sosyal Haklar** çalışma alanından değil, yalnızca **Sosyal Haklar yönetimi** çalışma alanından kullanılabilir.
>
> Bir kayıt yılının ortasında Sosyal Haklar yönetimine geçerseniz, Sosyal Haklar yönetiminde tüm yıl için çalışan verilerini doğru şekilde yapılandırmanız gerekir. Bu şekilde, tüm yıl boyunca doğru raporlama bilgileri aldığınızdan emin olursunuz.

## <a name="getting-started"></a>Başlarken

1095 formlarının bilgilerini izlemek için önce bir veya daha fazla Ekonomik Bakım kapsamı grubu oluşturmanız gerekir. Bu gruplar aşağıdaki bilgileri gösterir:

- Bir çalışana sağlanan kapsam teklifi
- Maliyet federal yoksulluk sınırının üzerindeyse, çalışanın en düşük maliyetli aylık prim payı
- Varsa işveren tarafından kullanılan Safe Harbor

Ekonomik Bakım kapsamı grupları, aynı koşullara sahip birden çok çalışan kaydı için bu bilgileri yönetmenize yardımcı olur. Bir veya daha fazla çalışana kolayca grup atayabilirsiniz.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Ekonomik Bakım kapsama grubu oluşturma veya düzenleme

1. **Sosyal Haklar yönetimi** çalışma alanında, **Ekonomik Bakım kapsamı grubu**'nu seçin.

    ![Ekonomik Bakım kapsamı grubunu seçme.](./media/hr-benefits-management-aca-coverage-group.png)

2. Yeni bir Ekonomik Bakım kapsamı grubu oluşturmak için **Yeni**'yi veya var olan bir grubu değiştirmek için **Düzenle**'yi seçin.

    ![Yeni veya Düzenle'yi seçme.](./media/hr-benefits-management-aca-new.png)

3. Aşağıdaki alanları ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Kuruluş adı | Grup için bir ad girin. |
    | Tanım | Grubun açıklamasını girin. |
    | Kapsam teklifi | Çalışanlara, eşlerine ve bakmakla yükümlü oldukları kişilere sunulan kapsam. |
    | Personel maliyet payı | Çalışanın sorumlu olduğu tutar. |
    | Geçerli bölüm 4980H güvenli liman | 4980H Safe Harbor veya geçiş desteği kodu. |
    | Plan başlangıç ayı | Sosyal hak planı yılınızın başladığı zamanın takvim ayını seçin. |
    | Grup geçerlilik başlangıcı | Bu kaydın geçerli olduğu ilk tarih. |
    | Grup geçerliliği sonu | Bu kaydın geçerli olduğu son tarih. Sona erme tarihi yoksa **Hiçbir Zaman** girin. |

    ![Kapsam grubu oluşturma.](./media/hr-benefits-management-aca-new-group.png)

4. **Kaydet**'i seçin.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Ekonomik Bakım kapsamı grubuna birden fazla çalışan atama

1. **Sosyal Haklar yönetimi** çalışma alanında, **Ekonomik Bakım kapsamı grubu**'nu seçin.
2. Çalışanların atanacağı grubu seçin.
3. **Toplu atama**'yı seçin.

    ![Toplu atamayı seçme.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Listeden çalışanları seçin ve sonra **Ata**'yı seçin.

    ![Seçilen çalışanları bir gruba atama.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Kapsama seçeneklerinin birden fazla sürümünü tutma

Bir kapsama grubunun birden fazla sürümünü tutabilirsiniz. Kuruluşunuzda veya sunulan sosyal haklarda bir değişiklik olduğunda, yeni bir grup oluşturmak ve çalışanları yeniden atamak zorunda kalmadan grubun bilgilerini güncel tutabilirsiniz.

Ekonomik Bakım kapsamı grupları oluşturduktan sonra, çalışanları bu gruplara toplu olarak atayabilirsiniz. Ayrıca, çalışanları gruplara tek tek atayabilir ve ACA bilgilerinin izlenip izlenmeyeceğini ve raporlanıp raporlanmayacağını belirtebilirsiniz.

Bir çalışanın ACA bilgilerini izlemeniz ve raporlamanız gerekmiyorsa **Rapor kapsamı** seçeneğini **Hayır** olarak ayarlayabilirsiniz. Örneğin, ACA raporlaması gerektirmeyen yarı zamanlı çalışanlarınız olabilir.

### <a name="override-default-values-for-an-employee"></a>Çalışan için varsayılan değerleri geçersiz kılma

Ekonomik Bakım kapsamı grubuna atanan çalışanlar için farklı değerler gerektiren herhangi bir ayda aşağıdaki seçenekleri değiştirebilirsiniz:

- Kapsam teklifi
- Personel maliyet payı
- Geçerli bölüm 4980H güvenli liman

> [!NOTE]
> 2020 ACA raporları için Form 1095-C'de hem iş hem de ev adresi posta kodlarını bildirmeniz gerekir. Değerler, geçerli etkin konumlara göre otomatik olarak doldurulur. Bir konum, yılın herhangi bir bölümünde farklıysa değeri geçersiz kılmanız gerekir. 1095-C raporunun **Posta Kodu** alanı (satır 17) yalnızca **Kapsam teklifi** kodu aşağıdaki gibi **1L** ile **1Q** arasında değer içeriyorsa doldurulur:
>
> - **1L, 1M veya 1N:** Birincil ikamet posta kodu
> - **1O, 1P, 1Q:** Birincil iş adresi posta kodu

Ekonomik Bakım kapsamı grubunun herhangi bir değeri için özel durumlar girmek istiyorsanız bu adımları izleyin.

1. **Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin ve sonra **Çalışanlar**'ı seçin.
2. Listeden çalışanı seçin.
3. **İstihdam** sekmesinde, **Daha fazla bilgi** bölümünde E **konomik Bakım kapsamı**'nı seçin.

    ![Bir çalışan için seçenekleri değiştirme.](./media/hr-benefits-management-aca-change-single-employee.png)

4. **Düzenle** öğesini seçin.
5. Değişiklik gerektiren her ay için **Varsayılanı geçersiz kıl** onay kutusunu seçin ve diğer değerleri gerektiği gibi değiştirin.

    ![Varsayılan değerleri geçersiz kılma.](./media/hr-benefits-management-aca-override-default.png)

6. **Kaydet**'i seçin.

## <a name="report-health-care-coverage"></a>Sağlık bakımı kapsamasını raporlama

Tam zamanlı ve yarı zamanlı çalışanlar için işveren destekli, kendi kaynaklarından teminat ayırma sigortalı sağlık hizmeti kapsamını izlemeniz gerekir. Her çalışanı, bakmakla yükümlü oldukları kişilerle birlikte, kapsandıkları aylar için 1095-C raporuna dahil edin.

Bir sosyal hak planının raporlanıp raporlanmayacağını belirtmek için şu adımları izleyin.

1. **Sosyal hak yönetimi** çalışma alanında, **Sosyal hak planları**'nı seçin.
2. Raporlanacak sosyal hak planını seçin.
3. **Düzenle** öğesini seçin.
4. **Ekonomik Bakım Yasası kapsamında bildiriliyor** seçeneğini **Evet** olarak ayarlayın.

    ![Sağlık bakımı kapsamasını raporlama.](./media/hr-benefits-management-aca-report-coverage.png)

5. **Kaydet**'i seçin.

Bir çalışan, bakmakla yükümlü olduğu bir kişi için sağlık hizmeti kapsamını seçerse bakmakla yükümlü olduğu kişinin kapsama süresi, bu kişinin kaydedildiği veya kaldırıldığı tarihe göre belirlenir. Bakmakla yükümlü olunan kişiler için kapsam tarihleri, bu kişinin kayıt yılı boyunca bir planda uygun ve etkin olduğu döneme göre otomatik olarak hesaplanır.

## <a name="generate-1095-b-and-1095-c-forms"></a>1095-B ve 1095-C formları oluşturma

ACA 1095-B ve 1095-C formları oluşturabilir ve bunları çalışanlarınızın her birine dağıtabilirsiniz. Internal Revenue Service'e (IRS) göndermek için Form 1095-C ve ilgili 1094-C iletim dosyalarını elektronik olarak oluşturabilirsiniz.

1. **Sosyal haklar yönetimi** çalışma alanında, **ACA 1095-B formu** veya **ACA 1095-C formu**'nu seçin.
2. Gerekirse parametreleri değiştirin ve sonra **Tamam**'ı seçin.

    > [!NOTE]
    > 500'den fazla çalışan için 1095-C formları yazdırıyorsanız birden fazla PDF dosyası alırsınız. **Belge yönetimi parametreleri** sayfasındaki **Megabayt cinsinden maksimum dosya boyutu** alanının değerini **150**'ye çıkarmanızı öneririz. (Bu sayfayı hızlı bir şekilde açmak için gezinti çubuğundaki arama alanını kullanın.)
    >
    > ![Maksimum dosya boyutunu değiştirme.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Raporlarınızın durumunu denetlemek ve görüntülemek için gezinti çubuğundaki arama alanını kullanarak **Elektronik raporlama işleri** sayfasını açın.

    ![Elektronik raporlama işleri sayfasını arama.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Görüntülenecek raporu seçin ve sonra **Dosyaları göster**'i seçin.

    ![Dosyaları gösterme.](./media/hr-benefits-management-aca-show-files.png)

5. **Aç**'ı seçin.

    ![Dosya açma.](./media/hr-benefits-management-aca-open-file.png)

6. Tarayıcı penceresinin altında görünen Bildirim çubuğundan zip dosyasını açın ve raporu seçin. PDF dosyasını görüntüleyebilir veya yazdırabilirsiniz.

    ![Örnek 1095-C formu.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>ACA kapsamı bilgilerini görüntüleme

**Çalışan Ekonomik Bakım kapsamı** sayfasında aşağıdaki bilgiler gösterilir:

- Her kapsam grubuna atanan çalışanlar
- Rapora dahil edilmesi gerekmeyen çalışanlar
- Atanmamış çalışanlar

Bu bilgileri görüntülemek için aşağıdaki adımları izleyin.

1. **Sosyal Haklar yönetimi** çalışma alanında, **Çalışan Ekonomik Bakım kapsamı**'nı seçin.
2. **Grup adı** alanından bir grup seçin.

    ![ACA kapsamını görüntüleme.](./media/hr-benefits-management-aca-view-coverage.png)

Ekonomik Bakım kapsama grubundaki varsayılan değerlerden herhangi biri geçersiz kılınmışsa değiştirilen değerin yanında bir yıldız işareti görünür. 12 ayın tamamı için değerler aynı ise ve geçersiz kılınmamışsa, değer **Tüm 12 ay** sütununda görünür.

ACA tarafından raporlanamayan ve Form 1095-C gerektirmeyen çalışanları görüntüleyebilirsiniz. **Filtreleme ölçütü** alanında, **ACA raporlanabilir değil**'i seçin.

Bir gruba atanmamış veya süresi dolmuş bir gruba atanmış çalışanları görüntüleyebilirsiniz. **Filtreleme ölçütü** alanında **Atanmamış veya süresi dolmuş grup** öğesini seçin.

### <a name="export-to-excel"></a>Excel'e aktar

Listelerden herhangi birini Microsoft Excel'e dışarı aktarmak için şu adımları izleyin.

1. **Microsoft Office'te Aç** düğmesini seçin.
2. Dahili kullanım için **HCM Human Resources geçici tablosu**'nu seçin.
3. **İndir**'i seçin.

### <a name="view-aca-reportable-dependents"></a>ACA tarafından raporlanabilir bakmakla yükümlü olunan kişileri görüntüleme

Kendi kaynaklarından teminat ayırmayla sigorta kapsamı sağladığınız için kapsanan kişileri bildirmeniz gerekiyorsa **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları kapsamındaki bakmakla yükümlü olunan kişileri görüntüleyebilirsiniz. Eylem bölmesinde, **Bakmakla yükümlü olunan kişi kapsamı**'nı seçin.

![Bakmakla yükümlü olunan kişi kapsamını görüntüleme.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Çalışanın bakmakla yükümlü olduğu kişilerin kapsam bilgileri gösterilir.

![Bakmakla yükümlü olunan kişi kapsamı.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Sayfa yalnızca **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planlarını gösterir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
