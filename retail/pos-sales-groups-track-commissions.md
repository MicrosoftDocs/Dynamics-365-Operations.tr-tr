---
title: "Komisyonlar, POS satış gruplarını kullanarak izleme"
description: "Müşteriyle çalışılan ilişkilendirme göre satışları izlemek için ortak bir perakende yöntemi olan — Yardım sağlayan yukarı satan, çapraz satış ve hareket işleme."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Komisyonlar, POS satış gruplarını kullanarak izleme

Müşteriyle çalışılan ilişkilendirme göre satışları izlemek için ortak bir perakende yöntemi olan — Yardım sağlayan yukarı satan, çapraz satış ve hareket işleme.

Satış temsilcisi tarafından satış izleme yeteneklerini satan associates ölçüsüdür, kasiyer tarafından satış sırasında hız ve verimlilik ölçüsüdür. Satış temsilcisi tarafından izlenen satış komisyonları veya diğer özendirme hesaplamak için de sık sık kullanılır.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>POS içinde bir satış temsilcisi olarak çalışan bir yapılandırma
Bir çalışan için bir satış grubu eklendiğinde, komisyon için uygun hale ve sistem içinde bir satış temsilcisi tanımlanabilir. Satış grubunda olmayan bir alt Komisyon için uygun değildir ve satış (POS) uygulamasının noktasında satış temsilcisi olarak listelenmez. POS satış temsilcilerinin listesi içeren en az bir alt mağazaya atanmış tüm satış grupları türetilir. Liste içinde POS satış grup kimliği ve adı birleşimi gösterilir (ID: adı). Varsayılan satış grubu işçilere nerede perakende satış temsilcisi POS satırlarına otomatik olarak ayarlamak için seçer senaryoları desteklemek için atanabilir. Kullanıcılar alt üyesi olan tüm satış grubu seçebilirsiniz.

## <a name="functionality-profile-settings"></a>İşlev profil ayarları
Akış ve POS satış temsilcilerinin ilgili işlemde belirleyecek bir mağazanın işlevselliği profil ayarları vardır.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Bu seçenek etkinleştirilirse, POS otomatik olarak geçerli kasiyer'ın varsayılan satış grubu ile hareket satırlarını doldurun. Bir kasiyer belirtilen varsayılan satış grubu yoksa, değeri olarak olmaz. Kullanıcı yine de el ile satış grubu POS düğme kılavuz düğmesini kullanarak ayarlayabilirsiniz.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Bu seçenek üç olasý deðeri vardýr: ** Hayır **-satış grubu seçmek için bu seçenek seçili ise, kullanıcı istenmez. Değer hala kasiyer'ın varsayılan satış grubu kullanılarak ayarlanabilir veya el ile bir POS kullanarak kılavuz düğmesinde. **Hareketin başlangıç** - bu seçenek seçili ise ve her iki **kasiyer için varsayılan** seçeneği etkin deðildir veya geçerli kasiyer bir varsayılan satış grubu yoksa, her hareket başına satış grubu seçmek için kullanıcıdan istenir. Satış grubu seçerek bu İstemi'nden sonraki satırları seçili satış grubu için varsayılan olarak ayarlanır. Kullanıcı yine de el ile satış grubu POS düğme kılavuz düğmesini kullanarak ayarlayabilirsiniz. **Her satır için** - bu seçenek seçili ise ve her iki **kasiyer için varsayılan** seçeneği etkin deðildir veya geçerli kasiyer bir varsayılan satış grubu yoksa, her satırı ekledikten sonra bir satış grubu seçmek için kullanıcıdan istenir. Kullanıcı yine de el ile satış grubu POS düğme kılavuz düğmesini kullanarak ayarlayabilirsiniz. |
| **İste**                           | Bu seçenek yalnızca POS satış temsilcisi için isteyecek şekilde yapılandırıldığında geçerlidir. Etkinleştirilirse, kullanıcı devam etmeden önce bir satış grubu seçmek için gerekir. Aksi takdirde, kullanıcı istenir, ancak iptal etmek ve bir seçim yapmadan devam edebilirsiniz. Satır eklendikten sonra yeterli izinlere sahip bir kullanıcı hala satış grubu satırından kaldırabilirsiniz. Bu durumda, "satış temsilcisi iste" zorlanmaz.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Satış Temsilcisi bilgileri POS hareketleri ekranda görüntüleme
POS hareket ekran düzeni ve içerik depoları, kayıtları veya çalışanlar için ekran düzeni tasarımcısı ve atanan ekran düzenleri kullanılarak yapılandırılabilir. **Satış temsilcisi** alan giriş bölmesi için satırları sekmesi eklenebilir.  Bu her satır için belirtilen satış grubu Kimliğini hareket ekranda görüntüler.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Ekleme satış temsilcisi operasyonlara POS ızgaralar düğmesini
POS ekran düzenleri POS işlemlerine erişim sağlamak için eklenen düğme grupları yapılandırmak kullanıcılara izin verir. Aşağıdaki işlemleri POS satış temsilcileri için ilgilidir düğme grubu düğmeleri atanabilir.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operasyon**                             | **Description**                                                                                                                                                                                                                                                                              |
| Satırdaki satış temsilcisini ayarla          | Bu POS işlemi uygun satış gruplarının bir listesini görüntüler (ID: ad) mağaza için. Bu listeden bir satış grubu seçerek değeri üzerinde geçerli hareket satırını ayarlayın.                                                                                                            |
| Satırdaki satış temsilcisini temizle        | Bu POS işlemi geçerli hareket satırından geçerli satış grubu değeri kaldırır.                                                                                                                                                                                                  |
| Set hareketinde satış temsilcisi   | Bu POS işlemi uygun satış gruplarının bir listesini görüntüler (ID: ad) mağaza için. Bu listeden bir satış grubu seçerek varsayılan değer geçerli hareket için ayarlayın. Atanmış bir satış grubu olmadan varolan satırları kümesi gibi sonradan eklenen tüm satırlar olacaktır. |
| Hareket üzerindeki Clear satış temsilcisi | Bu POS işlemi geçerli hareketin geçerli varsayılan satış grubu değeri kaldırır. Hareket zaten varolan satırları etkilemez.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisyonların hesaplanması
Komisyon işçi belirtilen satış grupları ekstre deftere nakli veya satış siparişi deftere nakil zamanında hesaplanır. Komisyon tutarı satış grubu ve müşteri ve/veya ürünleri hareketinde ilişkili Komisyon hesaplama ayarlarını tanımlandığı şekilde arkadaşlarınızdan birinin komisyon paylaşımında göre belirlenir.


