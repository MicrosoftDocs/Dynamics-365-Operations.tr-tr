---
title: Kazanç yönetimi çalışma alanı
description: Bu konuda, Dynamics 365 Human Resources'daki Kazanç yönetimi çalışma alanı açıklanmaktadır.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e7f606ae3c5c0a66764cc3235837380725241f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690041"
---
# <a name="benefits-management-workspace"></a>Kazanç yönetimi çalışma alanı


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Bu konuda, Dynamics 365 Human Resources'daki **Kazanç yönetimi** çalışma alanı açıklanmaktadır.

> [!NOTE]
> **Kazanç yönetimi** çalışma alanını görüntülemek için önce Özellik yönetiminde **(Önizleme) Kazanç yönetimi çalışma alanı** özelliğini etkinleştirmeniz gerekir. Önizleme özelliklerini etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).<br><br>![Kazanç yönetimi çalışma alanını etkinleştirme.](./media/hr-benefits-management-workspace-enable.png)

**Kazanç yönetimi** çalışma alanı, dikkatinizi gerektiren kazanç öğelerinin hızlı bir görünümünü sunar. Bu sayfada şunları görebilirsiniz:

- Eylem bekleyen öğelerin toplamları
- Onaylanmamış seçimleri olan çalışanlar
- Yakın zamanda sosyal yardımlara kaydolan çalışanlar
- Gelecekteki yaşam olayları olan çalışanlar
- Kayıtlı olmayan yeni işe alımlar
- Aktif yaşam olayları olan çalışanlar
- Herhangi bir plan seçmemiş açık kaydı olan çalışanlar

![Kazanç yönetimi çalışma alanı.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Eylem öğelerini görüntüleme

Bir kutucuk veya sekme seçerek eylem öğelerinizi görüntüleyebilirsiniz. Bir sekme seçerseniz çalışma alanı sayfasından çalışanları görüntüleyebilir ve seçebilirsiniz.

![Eylem öğeleri.](./media/hr-benefits-management-workspace-action-items.png)

Bir kutucuk seçerseniz o alanın sayfasına yönlendirilirsiniz. Örneğin, bu kutucuklardan herhangi birini seçmek, üzerinde işlem yapmanız gereken çalışanlar için filtrelenmiş **Çalışan kazanç planları** sayfasını görüntüler:

- **Onaylanmayan seçimler**
- **Kullanıma alınmış planların olmadığı kayıtları aç**
- **Kazançlara kaydedildi**
- **Yeni işe alınan kişi kayıtlı değil**

![Çalışan kazanç planları.](./media/hr-benefits-management-workspace-plans.png)

**Etkin yaşam olayları** veya **Gelecekteki yaşam olayları** kutucuklarını seçmek sizi etkin veya gelecekteki yaşam olayları listesine götürür.

![Yaşam olayları.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>İşleniyor

Kayıt uygunluğunu, yaşam olaylarını veya fiyat değişikliği güncelleştirmelerini işlemek için gezinti çubuğunda uygun öğeyi seçin.

![İşleniyor.](./media/hr-benefits-management-workspace-processing.png)

İşlemin sonuçlarını görmek için sayfadan **İşlem sonuçları**'nı seçin.

![İşlem sonuçları.](./media/hr-benefits-management-workspace-process-results.png)

Kazanç işleme hakkında daha fazla bilgi için bkz:

- [Kayıt uygunluğunu işleme](hr-benefits-process-enrollment-eligibility.md)
- [Yaşam olayı değişikliklerini işleme](hr-benefits-process-life-event-changes.md)
- [Yaşam olayı uygunluğunu işleme](hr-benefits-process-life-event-eligibility.md)
- [Yaşam olaylarını işleme](hr-benefits-process-life-events.md)
- [Oran değişikliklerini işleme](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Dönem değiştirme

Farklı bir kazanç dönemini görüntülemek için **Dönem** açılır listesinden seçim yapın.

![Dönem değiştirme.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Açık kayıt sekmesi

Bir kutucuk veya sekme seçerek eylem öğelerini görüntüleyebilirsiniz. Bir sekme seçerseniz çalışma alanı sayfasında çalışanları görüntüleyebilir ve seçebilirsiniz.
**Açık kayıt** sekmesi, açık kayıt işlemi için anahtar ölçümleri sağlar. 

Açık kayıt ile ilgili bilgiler, **Kayıt başlangıç tarihi**'nden 30 gün önce görüntülenir. Bu, **Kayıt başlangıç tarihi** alanında **Kazanç yönetimi** > **Bağlantılar** > **Dönemler**'de **Dönemler** ayarında tanımlanır.  Bu ayarı değiştirmek için **Human Resources paylaşılan parametreleri** > **Kazanç yönetimi** > **Açık kayıt seçenekleri**'ne gidin ve **Sayısı** alanını güncelleştirin.  

**Açık kayıt** sekmesinde aşağıdaki bilgiler kullanılabilir:
 - Açık kayıt işlemini başlatmayan çalışanlar
 - İşlemde seçimleri olan çalışanlar
 - Seçim işlemini tamamlayan çalışanlar
 - Onaylanmayan seçimler

**Özet kutucukları**

- **Başlatılmadı**: **Başlatılmadı** kutucuğunda, kayıt işlemini başlatmayan çalışanların sayısı gösterilir. **Başlatılmadı** kutucuğu yalnızca açık kayıt plan dönemi için seçilen, feragat edilen veya kullanıma alınan planlara sahip olmayan çalışanları gösteren filtrelenmiş bir listedir. Personel için varsayılan olarak seçildiklerinden zorunlu planlar dikkate alınmaz ve dahil edilmez.  **Çalışan kazanç planı** sayfasında açık kayıt işlemini başlatmayan çalışanların listesini görmek için bu kutucukta detaya inebilirsiniz.

  > [!NOTE]
  > **Plan türü** için açık kayıt ilerleme durumunu izlemek istemezseniz **Kazanç yönetimi** > **Bağlantılar** > **Personel self servis parametreleri** > **Kazanç planları kutucuk ayarı**'na gidip **Açık kayıt ilerlemesini izle** alanını güncelleştirerek bunu hariç tutabilirsiniz.  Örneğin, **Plan türü** = **Diğer** şeklinde oluşturulmuş planlara sahip olabilirsiniz. Bunlar, kayıt ilerleme durumunu izlemek istemediğiniz isteğe bağlı planlar olabilir. Bu plan türünü seçmezseniz bu tür planlar, **Açık kayıt** sekmesinde kayıt ilerleme veya tamamlanma durumunu izlerken yok sayılır. Bu ayar, tüm dönemler ve tüzel kişilikler için seçilen plan türüne uygulanır.

- **Devam ediyor**: **Devam ediyor** kutucuğunda, seçimleri devam eden çalışanların sayısı verilir. **Devam ediyor** kutucuğu yalnızca feragat edilen veya seçilen en az bir planı olan çalışanları gösteren filtrelenmiş bir listedir. Personel için varsayılan olarak seçildiklerinden zorunlu planlar dikkate alınmaz ve dahil edilmez. **Çalışan yan hak planlarını toplu olarak güncelleştirme** sayfasında seçilen ve feragat edilen planları görmek için bu kutucukta detaya inebilirsiniz.

- **Kazançlara kaydedildi**: **Kazançlara kaydedildi** kutucuğunda, kazançlara tamamen kaydedilen çalışanların sayısı verilir. **Kazançlara kaydedildi** kutucuğu, tümüyle seçilen veya feragat edilen planlara sahip çalışanları gösteren filtrelenmiş bir listedir. Sorgu, **Personel self servis parametreleri** sayfasında açık kayıt için izlenmeyen planları hariç tutar. **Çalışan kazanç planları** sayfasında çalışanların listesini görmek için bu kutucuktan detaya inebilirsiniz.

- **Onaylanmayan seçimler**: **Onaylanmayan seçimler** kutucuğunda, seçilen veya feragat edilen ve onaylanması gereken planlara sahip çalışanların sayısı gösterilir. **Çalışan yan hak planlarını toplu olarak güncelleştirme** sayfasında görüntülemek için bu kutucuktan detaya inebilirsiniz.

**Faaliyet**

- **Başlatılmadı**: **Başlatılmadı** sekmesinde, kayıt işlemini başlatmayan çalışanların listesi görüntülenir. **Başlatılmadı** kutucuğu, açık kayıt plan dönemi için seçilen, feragat edilen veya kullanıma alınan planlara sahip olmayan çalışanları gösteren filtrelenmiş bir listedir. Personel için varsayılan olarak seçildiklerinden zorunlu planlar dikkate alınmaz ve dahil edilmez. **Çalışan kazanç planları ayrıntısı** sayfasında görüntülemek için çalışanda detaya inebilirsiniz.

- **Seçimler devam ediyor**: **Seçimler devam ediyor** sekmesinde, seçimleri devam eden çalışanların listesi görüntülenir. **Seçimler devam ediyor**, feragat edilen veya seçilen en az bir planı olan çalışanları gösteren filtrelenmiş bir listedir. Personel için varsayılan olarak seçildiklerinden zorunlu planlar dikkate alınmaz ve dahil edilmez. **Çalışan kazanç planları ayrıntısı** sayfasında görüntülemek için çalışanda detaya inebilirsiniz.

## <a name="view-more-options"></a>Daha fazla seçenek görüntüleme

Daha fazla bilgi veya ek eylemleri görüntülemek için **Bağlantılar**'ı seçin.

![Bağlantılar.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Ayrıca bkz.

[Kazanç yönetimine genel bakış](hr-benefits-management-overview.md)
