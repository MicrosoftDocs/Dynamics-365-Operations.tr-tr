---
title: Ölçek birimi ambar iş yükü yüklendikten sonra işleme sorunları oluşuyor
description: Bu konu, ölçek birimi ambar iş yükü yüklendikten kısa bir süre sonra oluşabilecek sorunları açıklar ve bunları düzeltmek için tavsiyelerde bulunur.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071650"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Ölçek birimi ambar iş yükü yüklendikten sonra işleme sorunları oluşuyor

Bu konu, ölçek birimi ambar iş yükü yüklendikten kısa bir süre sonra oluşabilecek sorunları açıklar ve bunları düzeltmek için tavsiyelerde bulunur.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Sorun 1: Yük planlama çalışma alanından bir yük serbest bırakıldıktan sonra hata

### <a name="symptoms-of-issue-1"></a>Sorun 1'in belirtileri

**Yükleme planlama çalışma laanı** veya **Giden yük planlama çalışma alanı** sayfasından bir yük serbest bıraktığınızda, aşağıdaki şekilde bir hata iletisi alırsınız:

> %1 yükü deftere nakledilirken bir özel durumla karşılaştık. Yük, serbest bırakılamadı.
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> Sevkiyatlar'da (WHSShipmentTable) bir kayıt düzenlenemez. Sevkiyat Kodu: ...

Örnek verileri içeren gerçek bir örnek aşağıda verilmiştir:

> USMF-000033 yükü deftere nakledilirken bir özel durum yakalandı, yük serbest bırakılamadı.
oturum 5133 (Yönetici)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Scale Unit @@ @A Ölçek Birimine ait kayıtları güncellemeye çalıştı.  
> Nesne Sunucusu Azure:
>
> Sevkiyatlar'da (WHSShipmentTable) bir kayıt düzenlenemez. Sevkiyat Kimliği: USMF-000031, USMF-000033. SQL veritabanı bir hata verdi.

### <a name="cause-of-issue-1"></a>Sorun 1'in nedeni

Ölçek birimi ambar iş yükünü yüklediğinizde aşağıdaki koşul birleşimi varsa bu sorun oluşabilir:

- Sistem, birden çok satırın farklı siparişlerle ilişkili olduğu ve bazı yük satırlarının bir sevk irsaliyesiyle ilişkilendirilmemiş olduğu yayınlanmamış bir yük içerir.
- Sistem sevkiyat konsolidasyon kullanacak şekilde ayarlanmıştır.

Dağıtılmış karma topoloji dağıtımında, her yük ve sevkiyat kaydı belirli bir ölçek birimine veya hub'a ait olarak işaretlenir. **Yükleme planlama çalışma alanı** sayfasından bir yük serbest bıraktığınızda, sistem atanan sahipliği değiştirir. Ancak, daha önce listelenen koşullar nedeniyle, sistem veri sahipliğini çözemeyebilir. Bu nedenle, yükü ambara serbest bırakamaz.

### <a name="resolution-of-issue-1"></a>Sorun 1'in çözümü

Ambara serbest bırakmadan önce yükü iki küçük yüke bölün.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Sorun 2: Bir dalga ölçek biriminde işlenirken hata oluştu

### <a name="symptoms-of-issue-2"></a>Sorun 2'nin belirtileri

Ölçek birimindeki bir dalgayı işlerken, aşağıdaki şekilde bir hata iletisi alırsınız:

> Hala kurumsal hub'a ait olduğu için kayıt kimliği = %1, yük kimliği = %2 olan yükleme satırını değiştiremezsiniz. Lütfen karşılık gelen yükün bir ölçek birimine ve böylece oluşturulan ambar sipariş satırlarına serbest bırakıldığından emin olun.

Örnek verileri içeren gerçek bir örnek aşağıda verilmiştir:

> USMF-000000012 (9223377668365210) Dalgasını Yürüt işi için bilgi günlüğü  
> USMF-000000012 (9223377668370462) Dalgasını Yürüt görevi için bilgi günlüğü  
> Hala kurumsal hub'a ait olduğu için kayıt kimliği = 68719478242, yük kimliği = USMF-000034 olan yükleme satırını değiştiremezsiniz. Lütfen karşılık gelen yükün bir ölçek birimine ve böylece oluşturulan ambar sipariş satırlarına serbest bırakıldığından emin olun.

### <a name="cause-of-issue-2"></a>Sorun 2'nin nedeni

Dağıtılmış karma topoloji dağıtımında, yük ve sevkiyat verilerinin sahipliği belirli bir ölçek birimine veya hub'a atanır. Dalga işlemenin bir parçası olarak, verilerin sahipliğinin bir ölçek birimine atanması beklenir.

Bir ölçek birimi ambar iş yükü yüklediğinizde, açık bir sevkiyat, bir yük ve dalga ile ilişkilendirilirse, sistem veri sahipliğini denetleyemez. Bu nedenle, dalga işleme ölçek ünitesinde başarısız olur.

### <a name="resolution-of-issue-2"></a>Sorun 2'nin çözümü

Yükü hub'dan ambara serbest bırakın.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Kaydın sahipliğini ve hedefini görüntüleyerek sorunları giderme

Dağıtılmış karma topoloji dağıtımında, birçok kayıt türü belirli bir ölçek birimine veya hub'a ait olarak işaretlenir. Dağıtılmış karma topolojiye geçtikten ve/veya yeni bir ölçek birimi ambar iş yükü ayarladıktan sonra, sistem ilgili her kayda sahiplik atar. Bu işlem bazen hatalara veya beklenmeyen sonuçlara neden olabilir. Bu nedenle, bir kaydın sahipliği ve aktarım hedefi hakkındaki bilgiler, bu tür değişiklikleri yaptıktan sonra oluşan sorunları gidermenize yardımcı olabilir.

Bir kaydın sahipliğini ve aktarım hedefini görüntülemek için bu adımları izleyin.

1. İlgili kaydı açın.
1. Eylem Bölmesinde, **Seçenekler** sekmesindeki **Kayıt bilgileri** gurubunda **Tüm alanları göster**'i seçin.
1. Görüntülenen sayfa, seçili kayıt için kullanılabilen tüm alanların değerlerini gösterir. Şu alanları gözden geçirin:

    - **SYSSCALEUNITID** – Bu alanda kaydın geçerli sahibi gösterilir.
    - **SYSTARGETSCALEUNITID** – Bu alanda, geçerli sahibi onunla çalışmayı bitirdiğinde kaydın transfer edileceği hub veya ölçek biriminin ölçek birimi kimliği gösterilir. Bu alanın değeri, bu tür işlemleri yöneten toplu işlemler tarafından kullanılır. Bu alan doğrudan sahiplik ile ilgili olmasa da, kayıt aktarıldığında sahiplik değişebilir. Bazı durumlarda, bu alan boş olacaktır.
