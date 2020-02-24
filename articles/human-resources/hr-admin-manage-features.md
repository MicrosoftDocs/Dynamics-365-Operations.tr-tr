---
title: Özellikleri yönetme
description: Dynamics 365 Human Resources'ta yeni özelliklerin nasıl açıldığı veya kapatıldığını öğrenin.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010833"
---
# <a name="manage-features"></a>Özellikleri yönetme

Microsoft Dynamics 365 Human Resources için sürekli olarak kullanıma sunduğumuz yeni yeteneklerin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz. Neredeyse genel kullanıma hazır ve kapsamlı bir sınamadan geçirilmiş önizleme özelliklerini sunacağız. Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.

İnsan Kaynakları'ndaki yeni özellikler hakkında daha fazla bilgi için bkz. [İnsan Kaynakları'ndaki yenilikler](hr-admin-whats-new.md) ve [Dynamics 365 ve Power Platform Sürüm Planı](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.

Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

## <a name="enable-or-disable-preview-features"></a>Önizleme özelliklerini etkinleştirme veya devre dışı bırakma

Önizleme özelliklerine erişmek için, önce ortamınızda etkinleştirmeniz gerekir. Önizleme özelliklerini devre dışı bırakma veya etkinleştirme ortama özgüdür.

> [!IMPORTANT]
> Önizleme özellikleri yalnızca **korumalı alan** ortamlarında etkinleştirilecek. Önizleme özelliğini açtığınız zaman, kuruluşunuzda bulunan bu ortamdaki tüm kullanıcılar için etkinleştirmiş olursunuz. Önizleme özelliğini kapattığınız zaman devre dışı bırakmış ve kullanıcılarınızın erişimine kapatmış olursunuz. Önizleme özellikleri İnsan Kaynakları'nda sınırlı şekilde desteklenmektedir. Bu özellikler daha az gizlilik ve güvenlik önemi kullanabilir ve İnsan Kaynakları hizmet düzeyi sözleşmesine (SLA) dahil değildirler. Kişisel verileri (diğer bir deyişle, sizi tanımlamaya yardımcı olabilecek tüm bilgileri) işlemek ya da yasa veya düzenlemelerle uyumluluk gereksinimlerine tabi olan diğer verileri işlemek için önizleme özelliklerini kullanmamanız gerekir.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Özellik yönetimi** kutucuğunu seçin.

3. Bir önizleme özelliğini etkinleştirmek için, özelliği listeden seçin ve ardından **Etkinleştir**'i seçin. Bir önizleme özelliğini devre dışı bırakmak için, özelliği listeden seçin ve ardından **Devre dışı bırak**'ı seçin.

## <a name="preview-feature-benefits-management"></a>Önizleme özelliği: Kazanç yönetimi

Kazanç yönetimi size, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi ile birlikte, çok çeşitli kazanç seçeneklerini destekleyen esnek bir çözüm sağlar. Kazanç yönetimi yapılandırması ve kullanımı hakkında daha fazla bilgi için bkz. [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md).

Kazanç yönetimi, **Kazançlar** çalışma alanındaki işlevlerin yerini alıyor. Kazanç yönetimi önizleme özelliğini etkinleştirdiğiniz zaman, artık **Kazançlar** çalışma alanında şu formlara erişemezsiniz:

- **Kazançlar**
- **Kazanç öğeleri**
- **Katkı hesaplama oranları**
- **Kazanç kayıt sonuçları**
- **Kazanç geçerlilik süresini bitirme ve uzatma sonuçları**
- **Kazanç uygunluğu ilke kuralı türleri**
- **Kazanca uygunluk ilkeleri**
- **Uygunluk olayları**

Bu formlardaki bilgileri salt okunur modda görüntüleyebilirsiniz. Bilgileri düzenlemek isterseniz, önce Kazanç yönetimi önizleme özelliğini devre dışı bırakmanız gerekir.

### <a name="benefits-management-known-issues"></a>Kazanç yönetimiyle ilgili bilinen sorunlar

#### <a name="life-events"></a>Yaşam olayları

Yaşam olaylarını işleyen kullanıcı bir hata alacaktır:

Karşılama başlangıç tarihi, *plan döneminin başlangıcı* ile *plan döneminin sonu* arasında olmalıdır. 

Yaşam olayı, beklendiği gibi, işlenmeye devam edecek.

#### <a name="eligibility-processing"></a>Uygunluk işlemleri

1-5X maaş, Maaş Yüzdesi ve Sabit Tutar karşılama tutarı kullanan kazançlar için uygunluğu çalıştırırken, kazanç ayrıntıları tarihi **Çalışma geçmişi**'ndeki çalışan başlama tarihine ayarlanmalı, çalışılan saat sayısı, ödeme sıklığı ve yıllık kazançlar maaş tutarı da dahil edilmelidir. Çalışan için sabit ücret varsa, ödeme sıklığıyla birlikte çalışılan saatleri girin; yıllık maaş tutarı hesaplanacaktır. Çalışan maaşlı ise, çalışılan saatlere gerekmez. Yeni çalışanlar oluştururken önce sabit ücret girilmesini öneririz. Kazanç ayrıntıları kaydını güncelleştirmek için **Çalışan > Çalışan geçmişi > İstihdam ayrıntıları**'na gidin. Tarihi, çalışanın başlangıç tarihine ayarlayın.

#### <a name="employee-self-service"></a>Çalışan-self servis

Çalışanlar uygun olmadıkları ve bir plan seçip çıkabilirler. Örneğin bir çalışanın bakmakla yükümlü olduğu kişiler yoktur ama aile kapsamı seçeneği olan bir tıbbi plan seçebilir.

Hayat sigortası için karşılama tutarı güncelleştirilirken çalışan tutarı hesaplanmaz. Örneğin bir çalışana bir hayat sigortası planı sunulduğunda 1000 liralık karşılama tutarı başına 36 kuruşluk maliyetle 50.000 liraya kadar bir karşılama tutarı seçebilir.  Çalışan karşılama tutarını güncelleştirdiğinde, çalışanın ilişkili maliyeti sıfır olarak kalır.

Bu plan türünde yalnızca tek bir seçime izin veren bir kazanç planı için, bir plan seçtikten sonra bir planı feragat etmeye çalışırsa kullanıcı bir hata alır. Örneğin kullanıcı bir tıbbi plan seçip alışveriş sepetine ekliyor. Bunun ardından, başka bir tıbbi plan için **Feragat**'i seçiyor. Kullanıcı bir hata alacaktır.

## <a name="preview-features-in-leave-and-absence"></a>İzin ve devamsızlık'ta önizleme özellikleri

İzin ve devamsızlık önizleme özellikleri şunları içerir:

- **İzin ve devamsızlık takvimi** -İzin ve devamsızlık parametreleri, **İnsan kaynakları parametreleri**'nden, **İzin ve devamsızlık parametreleri** adlı yeni bir ekrana geçecek. Yeni ekranda yeni bir **Takvim** sekmesi var. Bu önizleme yalnızca parametrelerin bir alt kümesini sağlıyor. Yeni ekrana **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz. Takvimler şunları içerir:
  - **Şirket takvimi** -Tüm çalışan izin isteklerini gösterir. **İnsan kaynakları** rolündeki kişiler bu takvime **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirler.
  - **Yönetici ekibi takvimi** - Tüm bağlı çalışanların izin isteklerini gösterir. Yöneticiler takvime **İzin ve devamsızlık** altındaki Çalışan self servisi'ndeki **Ekibim** sekmesinden erişebilirler. 

- **İzin ve devamsızlık tatil takvimleri** - İzin türleri, çalışma zamanı takvimiyle birlikte kullanılan yeni bir **Tatil** seçeneği içeriyor. Tatiller ve kapanışlar ile tanımlanan günler artık çalışma günleri oluşturulurken **Tatil** olarak belirleniyor. Tahakkuklar işlenirken, çalışma gününe denk gelen tatilleri hesaba katmak için, takvime atanan çalışanlarda ayarlamalar yapılıyor.

- **İzin tahakkuku denetimi** - Yeni bir ekran, hem toplu olarak hem de tek tek çalışanların tahakkukları ne zaman işlediğini ve sildiğini incelemenizi sağlıyor. Bu yeni ekrana **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz.

- **İzin tahakkuku silme** - Artık belirli izin planları için tahakkuk kayıtlarını silebilirsiniz. Bu yeni seçeneğe **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz. Tek tek çalışanlar için bu seçenek, çalışan profilindeki **İzin ve devamsızlık** gruplandırmasında görüntülenir. 

- **İzin tahakkuku yuvarlama** - **İzin türü** için yeni seçenekler tahakkukta hangi tür yuvarlama kullanılacağını ve tahakkuk işlemi sırasında yuvarlamanın ondalık duyarlığını tanımlıyor. Tahakkuklar işlenirken, tahakkuk kayıtlarına yuvarlama ve duyarlık uygulanır. 

- **Tek bir izin planında birden fazla izin türü yapılandır** - İzin türleri için izin tahakkuku zaman çizelgesindeki yeni bir sütun, farklı tahakkuk zamanlamalarıyla bir izin ve devamsızlık planı üzerinde birden fazla izin türü tanımlamanıza olanak sağlıyor. Önceki **İzin türü** alanı kaldırıldı. Çalışan kaydında, izin türlerinin bakiyeleri şimdi ekranın üst bölümünde değil, bir tabloda görüntüleniyor.

  > [!IMPORTANT]
  > Bu özelliği etkinleştirildikten sonra kapatabilirsiniz.

- **Tahakkuk için bir çalışanın tam zamanlı eşdeğerliliğini (FTE) kullanımı** - İzin tahakkuku zaman çizelgesindeki yeni bir sütun, tahakkuk için FTE kullanmaya izin veriyor. Tahakkuklar işlenirken, uygulama, çalışanın birincil pozisyonunu ve orantılı tahakkuk tutarını belirlemek için tanımlanan FTE'yi kullanıyor.

  > [!NOTE]
  > Bu özellik ancak **Tek bir izin planında birden fazla izin türü yapılandır**'ı etkinleştirirseniz kullanılabilir. 

## <a name="feedback"></a>Bildirim

Bu önizleme özellikleriyle ilgili deneyiminizden haberdar olmak istiyoruz. Bu özellikleri veya diğer yeni özellikleri kullandıkça aşağıdaki sitelerden bize düzenli olarak geribildirim göndermenizi rica ediyoruz:

- [Topluluk](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Bu, kullanıcıların olayları tartışabileceği, sorular sorabileceği ve topluluktan yardım alabileceği yararlı bir kaynaktır.
- Üründe görmek istediğiniz özellikleri ve mevcut özellikler için yapmamız gerektiğini düşündüğünüz herhangi bir değişikliği bize bildirin. [İnsan Kaynakları fikirleri](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)'nde ürün fikirleri önerin
    
Lütfen kişisel verilerinizi (sizi tanımlamaya yardımcı olabilecek bilgileri) geri bildiriminize veya ürün incelemesi gönderimlerinize eklemeyin. Toplanan bilgiler daha ayrıntılı incelenebilir ve yürürlükteki gizlilik yasaları kapsamında talepleri yanıtlamak için kullanılamaz. Bu programlar altında ayrı olarak toplanan kişisel veriler [Microsoft Gizlilik Bildirimi](https://privacy.microsoft.com/privacystatement)'ne tabidir.

## <a name="see-also"></a>Ayrıca bkz.

- [İnsan Kaynakları'ndaki yenilikler](hr-admin-whats-new.md)
- [Dynamics 365 ve Power Platform Sürüm Planı](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)