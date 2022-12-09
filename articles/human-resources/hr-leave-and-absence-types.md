---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805217"
---
# <a name="configure-leave-and-absence-types"></a>İzin ve devamsızlık türlerini yapılandırma

[!include [preview banner](../includes/preview-banner.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta izin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir. İzin tiplerini kuruluşunuzun gereksinimlerine göre uyarlayabilirsiniz. İzin türleri örnekleri:

- Ücretli süre kesintisi (PTO)
- Ücretsiz izin
- Ücretli izin
- Hastalık izni
- Tıbbi izin
- Aile izni
- Kısa süreli engellilik
- Matem izni

## <a name="add-a-leave-type"></a>İzin türü Ekle

1. **İzin ve devamsızlık** çalışma alanında **Bağlantılar** sekmesini seçin.
2. **Kurulum** altında, **izin ve devamsızlık tipleri**'ni seçin.
3. **Yeni**'yi seçin.
4. **Tür** altındaki izin türü için ad girin, **Açıklama** altında bir açıklama girin ve **İş akışı kimliğinden** bir iş akışı seçin. İzin türüne bağlı olarak, **İstek türü** alanında bir istek türü seçin. Örneğin, **İzin** veya **Devamsızlık** öğesini seçin.
5. **Genel** olarak, **kategori** açılan menüsünde **yok**, **zamanlanmış** veya **zamanlanmamış** seçeneğini belirleyin.
6. **Kazanç kodu** açılan menüsünden bir kazanç kodu seçin.
7. **Neden kodu gerekli** olduğunda, neden kodu olmasını istiyorsanız bunu seçin. Neden kodları olmasını istiyorsanız, bunları eklemeniz gerekebilir. **Neden kodları** altında, **Ekle**'yi seçin, bir neden kodu seçin ve sonra da yanındaki **etkin** onay kutusunu seçin.
8. İstek türü **Devamsızlık izni** ise, aşağıdaki adımları izleyin:

      1. **Açık uçlu** altında, kullanıcıların açık uçlu izinler oluşturup oluşturmayacağını seçin.
      2. **Açık uçlu** etkinleştirilmişse, çalışanların devamsızlıktan döndüklerinde bir işe dönüş bildirimi göndermeleri gerekip gerekmediğini seçebilirsiniz.
      3. Çalışanların bir işe dönüş bildirimi göndermeleri gerekiyorsa **İşe dönüş bildirimini etkinleştir**'i etkinleştirebilirsiniz. **İşe dönüş bildirimini etkinleştir** etkinleştirilmişse, **Ek gerekli**  otomatik olarak etkinleştirilir ve devre dışı bırakılamaz.

9. Kullanıcıların, izin istekleri oluştururken veya güncelleştirdiklerinde karşıya belge yükleymeleri gerekiyorsa **Ek gerekli** seçeneğini etkinleştirebilirsiniz.
10. **Seçili rollere erişimi kısıtlamak** altında, erişimi kısıtlamak istediğinizi seçin. Sonra, **Bu izin türü için güvenlik rolleri** altında güvenlik rollerini seçin. Güvenlik rolleri, bu yordamda daha önce **iş akışı kodu** altında seçtiğiniz iş akışında tanımlanmıştır.
11. **Takvim rengi** altında, izin ve devamsızlık takvimlerinde bu izin türü için görüntülenecek rengi seçin.
11. **Askıya alma ilişkileri** altında , bu izin türünün başka bir izin türünü askıya alması veya başka bir izin türü tarafından askıya alınması gerekip gerekmediğini seçin. Askıya alma türü için devamsızlık yetkisi isteği gönderildiğinde, askıya alma türü için bir yeniden gönderme askıya alma işlemi otomatik olarak oluşturulur.
12. **Kaydet**'i seçin.

## <a name="configure-leave-type-rules"></a>İzin türü kurallarını yapılandırma

1. **İzin ve devamsızlık** türü için yuvarlama seçeneklerini ayarlayın. **Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır. Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.
2. İzin türü için **tatil düzeltmesi** ayarlayın. Bu seçeneği belirlediğinizde izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek üzere bir iş gününe denk düşen tatil sayısı kullanılır. Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.

   Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md).
   
 3. İzin türü için **ileriye doğru izin türü** ayarlayın. Bu seçeneği belirlediğinizde, tüm ileri düzey bakiyeleri belirtilen izin türüne aktarılır. İleriye yönelik izin türü de, bırak ve devamsızlık planına dahil edilmesi gerekir. 
 
4. İzin türü için **süre sonu kurallarını** tanımlayın. Bu seçeneği yapılandırdığınızda, gün veya ay birimini seçebilir ve bitiş tarihi için süreyi ayarlayabilirsiniz. Sona erme kuralının geçerlilik tarihi, izin süresinin dolmasını işleyen toplu işlemin ne zaman çalıştırılmaya başlayacağını veya kuralın ne zaman geçerli olacağını belirlemek için kullanılır. Süre sonunun kendisi her zaman tahakkuk dönemi başlangıç tarihinde gerçekleşir. Örneğin, tahakkuk dönemi başlangıç tarihi 3 Ağustos 2021 ise ve sona erme kuralı 6 ay olarak ayarlanmışsa, kural tahakkuk dönemi başlangıç tarihinden sona erme süresi mahsubu temel alınarak işlenir. Bu durumda 3 Şubat 2022'de yürütülecektir. Bitiş tarihinde varolan tüm izin bakiyeleri izin dışında bırakılacak ve bırakma bakiyesine yansıtılır.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>İzin türü başına gerekli eki yapılandırma

> [!NOTE]
> **Ek gerekli** alanını kullanmak üzere ilk olarak Özellik yönetiminde **İzin istekleri için gerekli eki yapılandırma** özelliğini açmanız gerekir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesinde, **Kurulum** altında **İzin ve devamsızlık türleri**'ni seçin.

2. Listeden bir **İzin ve devamsızlık türü** seçin. **Genel** bölümünde, bir çalışan seçili izin türü için yeni bir izin isteği gönderdiğinde ekin yüklenmesi gerekip gerekmediğini belirtmek için **Ek gerekli** alanını kullanın. 

Çalışanların, **Ek gerekli** alanının etkinleştirildiği bir izin türüne sahip yeni bir izin isteği gönderdiklerinde bir ek yüklemeleri gerekecektir. İzin isteği kapsamında yüklenen eki görüntülemek için izin isteğini onaylayanlar kendilerine atanan iş öğeleri için **Ekler** seçeneğini kullanabilir. Microsoft Teams'deki Human Resources uygulaması kullanılarak bir izin isteğine erişilirse izin isteği için **Ayrıntıları görüntüle** seçeneği, ayrıntılarını ve eklerini görüntülemek için kullanılabilir.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>İzin türü başına izin birimlerini (saat/gün) yapılandırma

> [!NOTE]
> İzin türü başına izin birimleri işlevini kullanmak üzere ilk olarak Özellik yönetiminde **İzin birimi başına izin birimlerini yapılandırma** özelliğini açmanız gerekir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

> [!IMPORTANT]
> Varsayılan olarak, bir tüzel kişilikteki izin türleri, izin parametrelerinin tüzel kişilik düzeyindeki yapılandırmasındaki izin birimlerini kullanır.
> 
> İzin ve devamsızlık türünün izin birimi, yalnızca bu izin türü için izin hareketi yoksa değiştirilebilir.
> 
> Özellik, açıldıktan sonra kapatılamaz.

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesinde, **Kurulum** altında **İzin ve devamsızlık türleri**'ni seçin.

2. Listeden bir izin ve devamsızlık türü seçin. Ardından, **Genel** bölümünde, **Birim** alanında, izin birimini seçin. **Saat** veya **Gün**'ü seçebilirsiniz.

3. İsteğe bağlı: **Birim** alanında **Saat**'i seçtiyseniz çalışanların yarım günlük izin istemeleri durumunda ilk yarım günü mü yoksa ikinci yarım günü mü seçebileceğini belirtmek için **Yarım gün tanımını etkinleştir** alanını kullanabilirsiniz.

Yeni bir izin isteği gönderen çalışanlar, izin isteklerini oluşturmak için farklı izin türleri seçebilirler. Ancak, tek bir izin isteğinin parçası olarak seçilen tüm izin türleri aynı izin birimine sahip olmalıdır. Çalışanlar, her izin türü için izin birimini **İzin isteme** formunda görüntüleyebilir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin ve devamsızlık planı oluşturma](hr-leave-and-absence-plans.md)
- [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)
- [İzni askıya al](hr-leave-and-absence-suspend-leave.md)
- [İzin satın alma ve satma isteği iş akışı oluşturma](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
