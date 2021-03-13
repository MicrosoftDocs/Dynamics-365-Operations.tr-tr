---
title: Ürün bilgileri ile ilgili sorunları giderme
description: Bu konuda, ürün bilgileri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007528"
---
# <a name="troubleshoot-product-information"></a>Ürün bilgileri ile ilgili sorunları giderme

Bu konuda, ürün bilgileri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.

## <a name="i-cant-delete-a-released-product"></a>Serbest bırakılan bir ürünü silemiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Serbest bırakılan bir ürünü ve tüm varyantlarını yalnızca serbest bırakılan ürünün ilgili işlemleri yoksa silebilirsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

Serbest bırakılmış bir ürünü veya ürün yöneticisini silmek için aşağıdaki adımları izleyin.

1. Maddeler için tüm açık hareketleri kapatın.
1. Stoğu 0'a (sıfır) düşürün.
1. Stok kapanışı gerçekleştirin.
1. Silmek istediğiniz ana ürün için tüm ürün varyantlarını silin.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Serbest bırakılan bir ürünün madde numarasını değiştirebilir miyim?

Çoğu durumda, bu değişiklik verilerin bozulmasına neden olacağından, serbest bırakılan ürünler için madde numaralarını değiştiremezsiniz. Madde numarasını, [platform güncelleştirmesi 24 ile Finance and Operations 10.0.0 için kaldırılan veya azaltılan özellikler](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) listesinde belirtildiği gibi, madde numarasını yalnızca serbest bırakılan ürünün birincil anahtarının önceki yeniden adlandırmanın neden olduğu veri bozulmasını onarmanız gerekiyorsa düzenleyebilirsiniz.

Serbest bırakılan ürünler için madde numaralarını da düzenlemek istiyorsanız [Fikirler portalında bu fikre oy verin](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Üründeki varsayılan otomatik tüketim kuralı, malzeme satırının faturasına girilmiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir maddeyi bir ürün reçetesi satırına eklediğinizde, sistem madde için ayarlanan varsayılan otomatik tüketim kuralı bilgilerini kullanmaz. Başka bir deyişle, maddeden otomatik tüketim kuralı **Ürün reçetesi satırı** sayfasında görünmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Bir ürün reçetesi satırında bir otomatik tüketim kuralı belirtirseniz bu, bu ürün reçetesi satırı için geçerli olacaktır. Ancak, otomatik tüketim kuralı boşsa veya ürün reçetesi satırına ayarlı değilse, madde üzerinde ayarlanan otomatik tüketim kuralı, ürün reçetesi satırında gösterilmese bile bu ürün reçetesi satırı geçerli olacaktır.

Microsoft Dynamics 365 Supply Chain Management'taki diğer özellikler için varsayılan mantık genellikle bu şekilde çalışmaz. Ancak geçerli davranış değiştirilemez. Aksi takdirde, buna dayanan bazı mevcut özelleştirmeler bozulabilir.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Sistem, yinelenen barkodları farklı maddeler veya farklı boyutlara sahip aynı madde için kaydetmemi sağlıyor.

Sistem şu anda benzersiz barkodları uygulamaz ve bu kısıtlamanın eklenmesi, bozulmaya neden olan bir değişiklik olacaktır. Öyle ki, Microsoft'un bazı mevcut müşteri yüklemelerinin bu değişiklik nedeniyle bozulacağını gösteren kanıtları vardır. Ancak, gelecekte bu özelliği etkinleştirmek için daha geniş bir tasarım değişikliği düşüneceğiz.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Madde kayıt şablonlarını düzenlerken aşağıdaki hata iletisini alıyorum: "Maddenin stoğu tutulmadığından ambar konumu oluşturulamıyor. Maddeleri stoklamak için ilişkili madde modeli grubundaki Stoğu tutulan ürün seçeneğinin seçilmesi gerekir."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, stoğu tutulmayan olmayan bir madde için şablon oluşturmaya çalışırken bu adımları izlerseniz oluşur.

1. Stoğu tutulmayan, serbest bırakılmış bir ürün açın.
1. Eylem Bölmesindeki **Seçenekler** sekmesinde, **Kayıt bilgileri**'ni seçin.
1. **Kayıt bilgileri** iletişim kutusunda **Şirket hesapları şablonu**'nu seçin.

Bu durumda aşağıdaki hata iletisini alırsınız:

> Maddenin stoğu tutulmadığından ambar konumu oluşturulamıyor. Maddeleri stoklamak için ilişkili madde modeli grubundaki Stoğu tutulan ürün seçeneğinin seçilmesi gerekir.

### <a name="issue-resolution"></a>Sorunun çözümü

Ürün şablonları oluşturma işlemi, ürüne özel ekstra mantık gerektirir. Bu nedenle, bu amaçla genel **Şirket hesapları şablonu** düğmesini kullanamazsınız. Bunun yerine, aşağıdaki adımları izleyin.

1. Serbest bırakılan bir ürün açın.
1. Eylem Bölmesinde **Ürün** sekmesinde **Yeni** grubunda **Şablon \> Paylaşılan şablon oluştur** öğesini seçin.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Ürün özniteliklerine eklenen Varsayılan Yardım metni, serbest bırakılmış bir ürüne girilmez.

Ürün özniteliklerine eklenen açıklama ve Yardım metni, serbest bırakılan ürünlerde görünmez veya varsayılan olarak girilen bir metin değildir. Bu davranış tasarımdan kaynaklanır.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Girilen varsayılan miktar, bir ürün reçetesinden kaydedildiğinde ve ürün reçetesinden kaydedildiğinde farklıdır.

### <a name="issue-description"></a>Sorun açıklaması

Varsayılan olarak, bir maddeyi bir ürün reçetesine eklediğinizde, seçili bir ürünün **Varsayılan sipariş ayarları** sayfasında **Min. sipariş miktarı** alanında tanımlanan miktar yerine miktar 1 olarak ayarlanır. Ancak, bir ürün reçetesi versiyonundan bir madde eklediğinizde ve madde ve varyant seçildiğinde, varsayılan olarak girilen miktar, belirli boyutlar için varsayılan sipariş ayarlarında ayarlanan minimum miktarı dikkate alır.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış beklenmektedir. Ancak, ürün reçetesi ile ürün reçetesi versiyonu arasında mantık farklı olması bilinen bir konudur. Yine de, bir değişiklik birçok farklı müşteri senaryosunu etkileyebileceğinden, bu davranış değiştirilmez.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Serbest bırakılan ürün ayrıntılarında, Ürün belge ekleri veri varlığından yüklenen ekli görüntüleri değiştiremiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, *Ürün belge ekleri* veri varlığını kullanarak bir öğeye görüntü eklediğinizde oluşabilir. Bu durumda, madde için madde görüntüsü gösterilir. Ancak, **Görüntüyü değiştir**'i seçerseniz, yüklenen görüntüler listesinde hiçbir şey gösterilmez. Ayrıca, madde için hiçbir ek gösterilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

*EcoResProductDocumentAttachmentEntity* varlığı (*Ürün belge ekleri*) *ürünler* için belge eklerini içeri aktarır ancak *serbest bırakılan ürünler* için aktarmaz. (Serbest bırakılan ürünler *maddeler* olarak da bilinir.) **Serbest bırakılan ürün ayrıntıları** sayfasında bir maddenin eklerini görüntülemek için bunun yerine *EcoResReleasedProductDocumentAttachmentEntity* varlığını *(Serbest bırakılmış ürün belgesi ekleri)* kullanmanız gerekir.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow bağlayıcısı aşağıdaki hata iletisini gösteriyor: "'ProductNumber' alanı için güncelleştirmeye izin verilmiyor."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, *Serbest bırakılan ürünler* varlığı V2 ve Microsoft Flow kullanılarak **Ürün numarası**'nı güncelleştirmeye çalıştığınızda oluşur.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış beklenmektedir. Serbest bırakılan bir ürünün ürün numarasını güncelleştirme özelliği, veri bozulmasını önlemeye yardımcı olmak için platform güncelleştirmesi 24'te Dynamics 365 Finance and Operations 10.0.0'dan kaldırılmıştır. Serbest bırakılmış bir ürünün birincil anahtarının önceki bir yeniden adlandırmanın neden olduğu veri bozulmasını onarmanız gereken özel durumlarda, Microsoft Destek'ten bu kısıtlamayı geçici olarak kaldırmasını isteyebilirsiniz.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Başka bir tüzel kişiliğe serbest bırakılmış bir ürün varyantı oluşturamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Varyantları olmayan bir ana ürünü serbest bırakmaya çalışır ve her tüzel kişide (şirket) varyantları gerektiği gibi oluşturursanız varyant önerilerini kullanarak varyantları serbest bırakamazsınız. Ayrıca varyantları el ile de oluşturamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Bir ana ürünün ilişkileri ve ana ürünün alabileceği boyutlar, ortak bir düzeyde tutulur. Bu nedenle, bu boyutların serbest bırakıldığı belirli bir tüzel kişilikte paylaşılan bir ana ürün için kullanılabilir boyutlar oluşturamaz ve boyutların gerekli olduğu her tüzel kişilikte işlemi kopyalayamazsınız. Bunun yerine, tasarlanan işleme uyum sağlamak için serbest bırakma işleminizi değiştirmeniz gerekir.

Ürünleri serbest bırakma işlemi burada verilmiştir.

1. Paylaşılan ana ürünü ve tüzel kişilere serbest bırakılabilecek boyutları oluşturun.
1. Ürünleri varyant önerilerini kullanarak veya serbest bırakılması gereken kombinasyonları el ile ekleyerek tüzel kişiliklere serbest bırakın.

Alternatif olarak, serbest bırakılan ürünü doğrudan oluşturabilirsiniz.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Başka bir şirkete bir varyant serbest bıraktığımda, aşağıdaki hata iletisini alıyorum: "Belirtilen boyutlardaki ürün çeşidi zaten oluşturuldu."

### <a name="issue-description"></a>Sorun açıklaması

Bir ürün varyantı A şirketine zaten serbest bırakılmışsa ve **Serbest bırakılan ürün varyantları** sayfasındaki **Yeni** düğmesini kullanarak B şirketine serbest bırakmaya çalışırsanız aşağıdaki hata iletisini alırsınız:

> Belirtilen boyutlardaki ürün çeşidi zaten oluşturuldu.

### <a name="issue-resolution"></a>Sorunun çözümü

**Serbest bırakılan ürün varyantları** sayfasındaki **Yeni** düğmesi varyantı oluşturur ve şirket bağlamında serbest bırakır. Varyant zaten oluşturulduysa **Yeni** düğmesini, başka bir şirkete serbest bırakma için kullanamazsınız.

Sorunu gidermek için **Ana ürün** sayfasını açın ve istenen şirketteki var olan varyantı serbest bırakmak için **Ürünü serbest bırak**'ı seçin.
