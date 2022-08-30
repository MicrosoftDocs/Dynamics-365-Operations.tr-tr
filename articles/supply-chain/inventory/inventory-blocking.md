---
title: Stok durdurma
description: Bu makalede, Supply Chain Management'ın kalite denetim sürecinin bir parçası olan stok engellemeye genel bakış sunulmuştur. Stok engellemeyi kullanarak maddelerin işlenmesini veya tüketilmesini engelleyebilirsiniz.
author: yufeihuang
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83b5417dc24af85f09e6713f2b12fdc358f61d54
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334700"
---
# <a name="inventory-blocking"></a>Stok durdurma

[!include [banner](../includes/banner.md)]

Bu makalede, Supply Chain Management'ın kalite denetim sürecinin bir parçası olan stok engellemeye genel bakış sunulmuştur. Stok engellemeyi kullanarak maddelerin işlenmesini veya tüketilmesini engelleyebilirsiniz.

Stok maddelerini aşağıdaki şekillerde durdurabilirsiniz:

- El ile
- Kalite emri oluşturma
- Kalite emri oluşturan bir işlemi kullanma
- Stok durumu durdurmayı kullanma

## <a name="blocking-items-manually"></a>Maddeleri el ile durdurma

**Stok durdurma** sayfasında bir hareket oluşturarak bir miktar maddeyi durdurabilirsiniz. Yalnızca eldeki stok olarak mevcut olan maddeler el ile durdurulabilir. El ile engellenen miktarlar için, planlama etkinliklerinin beklenen girişlerin beklenen eldeki miktar olarak eklenip eklenmeyeceğine karar vermeniz gerekir. Beklenen girişler, inceleme tamamlandıktan sonra eldeki stok olarak kullanılabilir olması beklenen durdurulmuş maddelerdir. Beklenen tarihi koruyabilirsiniz. Varsayılan olarak, **Beklenen girişler** seçeneği, bir kalite emri aracılığıyla durdurulan maddeler için seçilir. **Stok durdurma** sayfasındaki hareketi silerek miktara uygulanan el ile durdurmayı iptal edebilirsiniz.

## <a name="blocking-items-by-creating-a-quality-order"></a>Bir kalite emri oluşturarak maddeleri durdurma

**Kalite emirleri** sayfasında bir kalite meri oluşturarak incelenmesi gereken maddeleri belirtebilirsiniz. Bir kalite emri oluşturduğunuzda, bir madde için belirttiğiniz miktar durdurulur. Bir kalite emriyle ilişkili olan örnekleme planı yalnızca incelenmesi gereken maddelerin miktarını denetler; durdurulan miktar kontrol edilmez. Kalite emrine girilen, miktar durdurulan miktardır; örnekleme planında belirtilene bakılmaksızın inceleme için gönderilmesi gerekir.

> [!NOTE]
> Toplu iş bitiş tarihi ve stok durumu bloke etme özelliklerini kullanmak Master planlama tarafından desteklenmez. Bu, Master planlama sırasında ortaya çıkabilecek Eldeki stoğun çift dışarıda tutulmasına neden olabilir. Süresi dolan toplu işleri durdurmak için stok durumu yerine toplu iş değerlendirme kodlarına güvenmenizi öneririz.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Kalite meri oluşturan bir işlem kullanarak maddeleri durdurma

Kalite işlemi bir maddenin incelenmesi gerektiğini belirtirse, bir miktar madde otomatik olarak durdurulur. Bu nedenle, bir kalite emri otomatik olarak oluşturulduğunda, kalite emriyle ilişkili olan madde örnekleme planı hem durdurulan madde miktarını hem de incelenmesi gereken miktarı denetler. **Madde örnekleme** sayfasında **Tam durdurma** seçilirse, örneğin bir satınalma siparişi satırındaki tüm miktar, madde örnekleme adedine bakılmaksızın inceleme sırasında durdurulur.

### <a name="example"></a>Örnek

Aşağıdaki örnekte, bir satınalma siparişi sevk irsaliyesi deftere nakledildiğinde bir kalite emri oluşturulur. **Kalite ilişkilendirmeleri** sayfasında, satınalma siparişi sevk irsaliyesi naklinin kalite emrini etkinleştiren işlem olduğunu belirtirsiniz.

|Ayar |Kullanıcı eylemi |Sonuç |
|----|---|---|
| Kalite ilişkilendirme, kalite emrinin satınalma siparişi sevk irsaliyesi deftere nakledildiğinde oluşturulması gerektiğini belirtir. Kalite emrinin madde örnekleme ayarı, satınalam siparişi satırındaki miktarın yüzde 10'unun incelenmesi gerektiğini belirtir. Ayrıca, madde örnekleme ayarında **Tam durdurma** seçili olduğundan, satınalma sipariş satırındaki tüm miktarın, incelenmeye gönderilen miktara bakılmaksızın, inceleme sırasında durdurulması gerekir. | Sevk irsaliyesi deftere nakledilir. | Kalite emri oluşturulur. Satınalma siparişi miktarının yüzde onu incelemeye gönderilir.  Satınalma sipariş satırındaki tüm miktar durdurulur. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Stok durumu durdurmayı kullanarak maddeleri durdurma

**Stok durumları** sayfasındaki **Stok durdurma** parametresini kullanarak hangi stok durumlarının durdurulacağını belirtebilirsiniz. Üretim emirleri, satış siparişleri, transfer emirleri, giden hareketler veya proje tümleştirmeleri için stok durumlarını durdurma durumları olarak kullanamazsınız. Giden iş için kullanılabilen stok durumuna sahip maddeleri kullanın. Maddelerin durumu **Arızalı** olduğunda ve bu maddeler üzerinde master planlama çalıştırıldığında, maddeler eksik olarak kabul edilir ve stok otomatik olarak yenilenir.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Hem stok durumu engelleme hem de kalite emri engellemeyi kullanan maddeleri engellerken dikkatli olun

**Stok durdurma** parametresi etkinleştirilmiş bir stok durumuna sahip stokla ilişkili bir kalite emri oluşturabilirsiniz. Bu durumda, kalite emri, stok durumu tarafından oluşturulana ek olarak bir stok durdurma kaydı oluşturur. Kalite emri stok durdurması **Beklenen girişler** parametresini etkinleştireceğinden, bu, stok durumu tarafından da engellenen fazladan *Sipariş edilen stok* hareketi oluşturur. Bu birleşim, oluşturulan stok hareketlerinin anlamını anlamada zorluklara yol açabilir çünkü toplam durdurulan miktar eldeki toplam miktarın üzerindeymiş gibi görünür. 1 parçayı örnek almak için oluşturulan bir kalite emri ile 10 adet A0001 maddesinin alınması örneğindeki hareketleri inceleyelim. Davranış ayrıca **Stok ve ambar yönetimi parametreleri** sayfasında **Sipariş edilen maddeleri rezerve et** seçeneğinin etkin olup olmadığına da bağlıdır.

>[!NOTE]
>Stok durumu engellemeyi ve kalite emirlerini birlikte kullanıyorsanız **Sipariş edilen maddeleri rezerve et** seçeneğinin etkinleştirilmesini kesinlikle öneririz.

### <a name="example-with-reserve-ordered-items-enabled"></a>"Sipariş edilen maddeleri rezerve et" etkin örneği

**Rezerve edilen maddeleri rezerve et** etkinleştirildiğinde, tüm stok durdurma hareketleri *Rezerve edilmiş fiziksel* veya *Rezerve edilmiş sipariş* durumuna sahip olur.

| Stok hareketi referansı | Giriş | Çıkış | Miktar | Tesis | Ambar | Stok durumu | Yer | Plaka | Yorum |
|---|---|---|---|---|---|---|---|---|---|
| Satın alma siparişi | Satın alınan | | 10 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | | 
| Stok durdurma | | Fiziksel rezerve miktar | -9 adet | 2 | 24 | Bloke etme | | | Stok durumu durdurma tarafından oluşturulan hareket |
| Stok durdurma | | Fiziksel rezerve miktar | -1 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | Kalite emri örnekleme durdurması tarafından oluşturulan hareket |
| Stok durdurma | Sipariş edilen | | 1 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | Kalite emri örnekleme durdurmadan beklenen girişler |
| Stok durdurma | | Siparişli rezerve miktar | 1 adet | 2 | 24 | Bloke etme | | | Stok durumu durdurma tarafından oluşturulan hareket

### <a name="example-with-reserve-ordered-items-disabled"></a>"Sipariş edilen maddeleri rezerve et" devre dışı örneği

**Sipariş edilen maddeleri rezerve et** devre dışı bırakıldığında, beklenen girişler *Sipariş edildi* durumunda olduklarından rezerve edilemez, bu nedenle bazı durdurmalar *Siparişte* durumunda bırakılır.

| Stok hareketi referansı | Giriş | Çıkış | Miktar | Tesis | Ambar | Stok Durumu | Yer | Plaka | Yorum |
|---|---|---|---|---|---|---|---|---|---|
| Satın alma siparişi | Satın alınan | | 10 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | |
| Stok durdurma | | Fiziksel rezerve miktar | -9 adet | 2 | 24 | Bloke etme | | | Stok durumu durdurma tarafından oluşturulan hareket |
| Stok durdurma | | Fiziksel rezerve miktar | -1 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | Kalite emri örnekleme durdurması tarafından oluşturulan hareket |
| Stok durdurma | Sipariş edilen | | 1 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | Kalite emri örnekleme durdurmadan beklenen girişler |
| Stok durdurma | | Siparişte | 1 adet | 2 | 24 | Bloke etme | ALND | receiptLp1 | Stok durumu durdurma tarafından oluşturulan hareket

İki durum arasındaki hareket durumu ve boyut farklılığına dikkat edin. Bu nedenle, **Sipariş edilen maddeleri rezerve et** seçeneğini etkinleştirmenizi öneririz.

## <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory"></a>Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak

Stok durumunun sonucu olarak gerçekleşen durdurulan stoktan örnek alan kalite emirleri durumunda stok hareketlerini basitleştirmek için sistem, bu tür kalite emirlerinden beklenen girişleri devre dışı bırakan bir özellik sağlar. Beklenen giriş stok durumu engelleme işlemi tarafından hemen engellendiğinden, bu değişiklik nedeniyle eldeki stokta bir azaltma olmaz.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla özellik varsayılan olarak açıktır. Yöneticiler, [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak* özelliğini bularak bu işlevi açabilir veya kapatabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Stok durdurma oluştur ve sürdür](tasks/create-maintain-inventory-blocking.md)

[Kalite yönetimi işlemleri](quality-management-processes.md)

[Malların kalitesini denetle](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]