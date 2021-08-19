---
title: Stok işlemlerinde sorun giderme
description: Bu konuda, stok işlemleri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceği açıklanmaktadır.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 1198bc12830afa2ae2c5eb8e77413a9d8ef70c625823f676ab1965ff250c2443
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730405"
---
# <a name="troubleshoot-inventory-operations"></a>Stok işlemlerinde sorun giderme

[!include [banner](../includes/banner.md)]

Bu konuda, stok işlemleri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceği açıklanmaktadır.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Stok günlükleri için "İş akışı" açılan iletişim kutusunu bulamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Günlük sayfasında **İş akışı** açılır iletişim kutusunu bulamazsınız veya ilgili iş akışı işlemleri kullanılamaz.

Bu sorun, aşağıdaki alt bölümlerde açıklandığı gibi, üç nedenden dolayı oluşabilir.

### <a name="issue-resolution-1"></a>Sorunun çözümü 1

Sorun tüm kullanıcılar için geçerliyse sorunun nedeni onay iş akışının günlük adına atanmaması olabilir. Sorunu düzeltmek için şu adımları izleyin.

1. **Stok Yönetimi &gt; Kurulum &gt;> Günlük adları &gt;> Stok** öğesine gidin.
1. Liste bölmesinde, ayarlarını açmak için bir günlük adı seçin.
1. **Genel** hızlı sekmesinde, **Onay iş akışı** seçeneğini *Evet* olarak ayarlayın. Değişikliği onaylamanız istendiğinde, **Evet**'i seçin.
1. **İş akışı** alanında, seçili günlük adı için kullanmak istediğiniz iş akışını seçin.

### <a name="issue-resolution-2"></a>Sorunun çözümü 2

İş akışınızda özelleştirilmiş kod kullanılıyorsa sistemi yükselttikten sonra sorunlar oluşabilir. Örneğin, günlük iş akışında **Gönder** düğmesi gri renkte olabilir. Bu nedenle, gönderimi onaylamak için düğmeyi seçemeyebilirsiniz.

**Gönder** düğmesi gri renkteyse iş akışınız özelleştirilmiş olabilir. Bu, `FormDataUtil` öğesindeki `canSubmitToWorkflow()` iş akışı yönteminin genişletildiği anlamına gelir. Bu sorunu gidermek için `canSubmitToWorkflow()` yöntemini genişletme şeklinizi aşağıdaki örnekte gösterilen yapıyı kullanarak değiştirin.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Sorunun çözümü 3

Sorun yalnızca belirli birkaç kullanıcı için geçerliyse bu kullanıcılar, stok günlüklerinde iş akışı işlemlerini çalıştırmak için gerekli güvenlik ayrıcalıklarına sahip olmayabilir. Etkilenen her kullanıcının *Stok günlüğü iş akışının bakımını yapma* güvenlik ayrıcalığına sahip olduğundan emin olun. Varsayılan olarak, bu ayrıcalık aynı adlı bir göreve atanır ve bu görev *Ambar çalışanı* ve *Ambar yöneticisi* rollerine uygulanır.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Stok günlüğüm sistem kilitli durumunda kalıyor ve iş akışı toplu işi çalışmıyor.

### <a name="issue-description"></a>Sorun açıklaması

Stok günlükleriniz bir işlem tarafından kilitlenmiş ve yayınlanmıyor. Örneğin, deftere nakil sırasında (bir sistem kilitleme işlemidir) bilinmeyen bir hata oluşursa günlük, sistem kilitli durumunda kalabilir. Bu durumda, iş akışı iş öğesi işleyicisi, kilit doğrulama işlemini gerçekleştirirken bir hata oluşturur.

### <a name="issue-resolution"></a>Sorunun çözümü

Supply Chain Management için SQL Server kurulumunda oturum açın ve **InventJournalTable.SystemBlocked** seçeneğinin *1* olarak ayarlanıp ayarlanmadığını kontrol edin. Bu şekilde ayarlanmışsa günlüğün kilitli durumda olmaması gerektiğinden emin olun ve ardından **InventJournalTable.SystemBlocked** seçeneğini *0* olarak ayarlayın.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Stok günlüğü iş akışım asla tamamlanmıyor ve günlük düzenlenemiyor ve nakledilemiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir günlük onay iş akışını gönderdikten sonra, iş akışı işlemesi yanıt vermemeye başlar ve günlüklerinizi düzenleyemez veya işleyemezsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

İş akışı işlemenin tamamlanmamasının birden fazla nedeni olabilir. Aşağıdaki sorunların olup olmadığını kontrol edin:

- **Stok yönetimi &gt; Kurulum &gt; Stok yönetimi iş akışları**'na gidin ve etkilenen iş akışının yapılandırmasını inceleyin. Daha fazla bilgi için bkz. [Stok günlüğü onay iş akışları](inventory-journal-workflow.md).
- İş akışı bir özel durum veya hata ile karşılaşıyor olabilir. Etkilenen iş akışının iş öğesi geçmişini gözden geçirerek iş akışını sonlandıran bir uygulama hatası içerip içermediğini inceleyin.
- Stok günlüğü yalnızca onaylanırsa güncelleştirilebilir veya düzenlenebilir. Geri çağırma etkinse, günlüğü geri çağırmayı deneyebilirsiniz. İş akışı toplu işinin yürütülmesi birden çok nedenle askıya alınabilir. Bu nedenlerden bazıları iş akışı çerçevesi sorunundan kaynaklanıyor olabilir.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Stok günlüğü iş akışı koşulları, satır düzeyinde değil, yalnızca günlük düzeyinde uygulanıyor

### <a name="issue-description"></a>Sorun açıklaması

Bu sorunla, maliyet tutarında stok günlüğü iş akışı koşulu ayarlamaya çalışmanız gibi durumlarda karşılaşabilirsiniz. 1. adımın yalnızca maliyet tutarı 100'den az olduğunda çalışması için bir koşul ayarlarsınız. Ardından 2. adımın yalnızca maliyet tutarı 100'e eşit veya daha fazla olduğunda çalışması için başka bir koşul daha ayarlarsınız. Ardından, iş akışı çalıştırıldığında iş akışı geçmişinde yalnızca tek satır gösterilir ve gönderilen değere bakılmaksızın, her zaman ilk koşul *true* olarak değerlendirilir.

### <a name="issue-workaround"></a>Sorun geçici çözümü

Geçerli sürümde, stok günlüğü iş akışı koşulları, satır düzeyinde değil, yalnızca günlük düzeyinde uyglanır. Bu davranış tasarımdan kaynaklanır. Koşul ölçütlerinizi yalnızca günlük düzeyi özniteliklerinde ayarlamanızı öneririz.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Eldekilerin listesi sayfasındaki filtre bölmesi sonuçları beklediğim şekilde filtrelemiyor.

### <a name="issue-description"></a>Sorun açıklaması

**Eldekilerin listesi** sayfasındaki filtre bölmesinde yer alan filtreler, sonuçları beklediğiniz şekilde filtrelemiyor.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır.

 **Eldekilerin listesi** sayfası, kullanılabilir tüm boyutları içeren ayrıntılı bir eldeki stok tablosundan toplanır. Ancak bu sayfadaki liste bir özettir. Bu nedenle, gösterilen boyutlara göre değerleri toplayarak kaynak tablodaki satırları birleştirebilir.

Filtre bölmesinde ayarlanan filtreler, toplanan listeye değil, kaynak tabloya uygulanır. Bu davranış, [bu örneklerde](inventory-on-hand-list.md#examples) gösterildiği gibi bazen beklenmeyen sonuçlar doğurabilir.

Ancak,  [ızgarada sağlanan filtreler](inventory-on-hand-list.md#grid-filters) toplanan liste için *geçerlidir* . Bu filtreler kılavuzun üst kısmındaki hızlı filtreyi ve her sütun başlığının filtresini içerir.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Birim ve birim miktarı stok günlüğünde doğru çalışmıyor.

### <a name="issue-description"></a>Sorun açıklaması

Stok günlüğünde birimlerle ve miktarlarla çalışırken aşağıdaki sorunlardan biriyle veya her ikisiyle birden karşılaşabilirsiniz:

- Serbest bırakılan ürün için bir dönüştürme birimi ayarlanırken stok günlüğünde birimleri veya birim miktarlarını görmezsiniz ve stok günlüğündeki birimi değiştiremezsiniz.
- Stok günlüğünde **Miktar** ve **Birim** alanlarını görürsünüz ancak **Birim miktarı** alanını görmezsiniz. Birimi değiştirir, bir miktar girer ve günlüğü deftere naklederseniz günlük, söz konusu miktar için özgün ölçü birimini göstermeye devam eder.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorunu düzeltmek için şu adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, *Stok günlüklerinde ölçü birimi ve birim miktarı kullanımı* özelliğinin açık olduğundan emin olun. Bu özellik, günlüğe **Birim** ve **Birim miktarı** alanlarını ekler.
1. Özellik etkinleştirildikten sonra **Miktar**, **Birim miktarı** ve **Birim** alanlarını aşağıdaki şekilde kullanın.

    - **Miktar**: Serbest bırakılan ürün için tanımlanan varsayılan birimi kullanarak miktarı belirtin. Ancak, varsayılan birimin kendisi burada gösterilmez. Varsayılan birim ile **Birim** alanında seçilen birim arasında dönüştürme işlemi ayarlandıysa, **Miktar** alanı **Birim miktarı** ve **Birim** alanlarındaki seçimlere göre otomatik olarak güncelleştirilir.
    - **Birim miktarı**: **Birim** alanında seçilen birimi kullanarak miktarı belirtin.
    - **Birim**: **Birim miktarı** alanındaki değere uygulanacak birimi seçin.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Şu hata iletisini alıyorum: "Stok tutma birimi için maksimum ondalık birim sayısı 0'dır."

### <a name="issue-description"></a>Sorun açıklaması

Bir stok hareketini veya stok rezervasyonunu deftere nakletmeye çalıştığınızda, şu hata iletisini alırsınız: "Stok tutma birimi için maksimum ondalık birim sayısı 0'dır."

Bu sorun stok hareketi miktarı, alanın desteklediği duyarlık düzeyinin altında olan bir ondalık değer olarak belirtildiğinde oluşur. Örneğin, bir stok hareketi için *0,5* miktarı belirtilmiştir ancak yalnızca tamsayı olan miktarlar desteklenmektedir. Bu nedenle, değer *0,5* yerine *1* olmalıdır.

### <a name="issue-resolution"></a>Sorunun çözümü

1. Stok hareketlerindeki miktarları yuvarlamak için SQL Server kurulumunuzda aşağıdaki kodu çalıştırın. Bu kod, **inventTrans** tablosundaki değerleri düzeltecektir.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. **Sorunu düzelt** seçeneğinin açık olduğu bir eldekiler tutarlılık denetimi çalıştırın. Bu denetim, **inventSum** tablosundaki değerleri düzeltecektir.

> [!IMPORTANT]
> Kodu ortam için gereken şekilde dikkatle düzenlemenizi, test ortamında test etmenizi ve kodu üretim ortamında çalıştırmadan önce sonuçta elde edilen verileri denetlemenizi önemle tavsiye ederiz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]