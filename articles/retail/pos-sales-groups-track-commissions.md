---
title: "Komisyonları POS'ta satış gruplarını kullanarak izleme"
description: "Satışları müşteriyle çalışan (yardım sağlayan, yukarı satış yapan, çapraz satış yapan ve hareketi işleme koyan) yetkiliye göre izlemek genel bir perakende yöntemidir."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 92963dff5703376ea44601434fc874728c92f813
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Komisyonları POS'ta satış gruplarını kullanarak izleme

[!INCLUDE [banner](includes/banner.md)]

Satışları müşteriyle çalışan (yardım sağlayan, yukarı satış yapan, çapraz satış yapan ve hareketi işleme koyan) yetkiliye göre izlemek genel bir perakende yöntemidir.

Satışları satış temsilcisine göre izleme yetkilinin satış kabiliyetlerine yönelik bir ölçüyken, kasiyere göre satışlar hız ve verimlilik ölçüsüdür. Satış temsilcisine göre izlenen satışlar sıklıkla komisyonları veya diğer teşvikleri hesaplamak için de kullanılır.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Bir çalışanı POS'ta satış temsilcisi olarak yapılandırma
Bir çalışan bir satış grubuna eklendiğinde, komisyon için uygun duruma gelir ve sistemde bir satış temsilcisi olarak tanımlanabilir. Satış grubunda olmayan çalışan komisyon için uygun değildir ve satış noktası (POS) uygulamasında satış temsilcisi olarak listelenmez. POS'ta satış temsilcilerinin listesi mağazaya atanmış en az bir çalışan içeren satış gruplarından türetilir. Liste POS'ta Satış grubu Kimliği ve Adı birleşimi (Kimlik : Adı) olarak gösterilir. Varsayılan satış grubu, perakendecinin satış temsilcisini POS hatlarında otomatik olarak seçtiği senaryoları desteklemek amacıyla çalışanlara atanabilir. Kullanıcılar, çalışanın üyesi olduğu herhangi bir satış grubundan seçim yapabilir.

## <a name="functionality-profile-settings"></a>İşlevsellik profili ayarları
POS'ta satış temsilcilerinin dahil olduğu akış ve süreci belirleyecek olan bir mağaza için çok sayıda işlevsellik profili ayarı vardır.


|                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              <strong>Profil</strong>              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        <strong>Açıklama</strong>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <strong>Mümkün olduğunda varsayılan olarak kasiyere geç</strong> |                                                                                                                                                                                                                                                                                                                                                                                                     Bu seçenek etkinleştirilirse, POS otomatik olarak geçerli kasiyerin varsayılan satış grubu ile hareket satırlarını doldurur. Bir kasiyerin belirtilen varsayılan satış grubu yoksa, değer ayarlanmaz. Kullanıcı yine de bir POS düğme grubu düğmesi kullanarak satış grubunu el ile ayarlayabilir.                                                                                                                                                                                                                                                                                                                                                                                                      |
|  <strong>Satış temsilcisi istemi</strong>  | Bu seçeneğin üç olası değeri vardır: <strong>Hayır **- Bu seçeneği seçerseniz, kullanıcıdan bir satış grubu seçmesi istenmez. Değer hala bir kasiyerin varsayılan Satış grubu kullanılarak veya POS düğme grubu düğmesi kullanılarak el ile ayarlanabilir. **Hareketin başlangıcı</strong> - Bu seçenek seçilirse ve <strong>Varsayılan olarak kasiyere geç</strong> seçeneği etkin değilse veya geçerli kasiyerin bir varsayılan satış grubu yoksa, kullanıcıdan her hareketin başında bir satış grubu seçmesi istenir. Bu istemden bir satış grubu seçmek sonraki tüm satırların seçili satış grubu için varsayılan olarak ayarlanmasını sağlar. Kullanıcı yine de bir POS düğme grubu düğmesi kullanarak satış grubunu el ile ayarlayabilir. <strong>Her satır için</strong> - Bu seçenek seçilirse ve <strong>Varsayılan olarak kasiyere geç</strong> seçeneği etkin değilse veya geçerli kasiyerin bir varsayılan satış grubu yoksa, kullanıcıdan her satır ekledikten sonra bir satış grubu seçmesi istenir. Kullanıcı yine de bir POS düğme grubu düğmesi kullanarak Satış grubunu el ile ayarlayabilir. |
|              <strong>İste</strong>              |                                                                                                                                                                                                                                                                                                                         Bu seçenek yalnızca POS satış temsilcisi isteyecek şekilde yapılandırıldığında geçerlidir. Etkinleştirilirse, kullanıcıdan devam etmeden önce bir satış grubu seçmesi istenir. Aksi takdirde, kullanıcıdan istemde bulunulur ancak kullanıcı isteği iptal edip herhangi bir seçim yapmadan devam edebilir. Satır eklendikten sonra, yeterli izinlere sahip kullanıcı satış grubunu satırdan kaldırabilir. Bu durumda "satış temsilcisi iste" için zorlama yapılmaz.                                                                                                                                                                                                                                                                                                                          |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Satış temsilcisi bilgilerini POS hareketleri ekranında görüntüleme
POS hareketi ekran düzeni ve içerikleri, ekran düzeni tasarımcısı ve mağazalara, kasalara veya çalışanlara atanan ekran düzenleri kullanılarak yapılandırılabilir. **Satış temsilcisi** alanı Giriş bölmesinin Satırlar sekmesine eklenebilir.  Bu, hareket ekranının her satırı için belirtilen Satış grubu kimliğini görüntüler.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Pos düğme gruplarına Satış temsilcisi işlemleri ekleme
POS, kullanıcılara POS işlemlerine erişim sağlamak amacıyla ekran düzenlerine dahil edilen düğme gruplarını yapılandırma olanağı sunar. Aşağıdaki POS işlemleri Satış temsilcileri ile ilgili olan düğme grubu düğmelerine atanabilir.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operasyon**                             | **Açıklama**                                                                                                                                                                                                                                                                              |
| Satırdaki satış temsilcisini ayarla          | Bu POS işlemi mağaza için uygun Satış gruplarının bir listesini görüntüler (Kimlik: Ad). Bu listeden bir Satış grubu seçmek geçerli hareket satırındaki değeri ayarlar.                                                                                                            |
| Satırdaki satış temsilcisini temizle        | Bu POS işlemi geçerli Satış grubu değerini geçerli hareket satırından kaldırır.                                                                                                                                                                                                  |
| Hareketteki satış temsilcisini ayarlama   | Bu POS işlemi mağaza için uygun Satış gruplarının bir listesini görüntüler (Kimlik: Ad). Bu listeden bir Satış grubu seçmek geçerli hareketteki varsayılan değeri ayarlar. Atanmış bir satış grubu olmayan mevcut satırlar ve sonradan eklenen satırlar ayarlanır. |
| Hareketteki satış temsilcisini temizleme | Bu POS işlemi geçerli varsayılan Satış grubu değerini geçerli hareketten kaldırır. Harekette zaten varolan satırları etkilemez.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisyonları hesaplama
Komisyon, belirtilen satış gruplarındaki çalışanlar için ekstrelerin deftere nakledilmesi veya satış siparişinin deftere nakledilmesi sırasında hesaplanır. Komisyon tutarı, satış grubunda ve hareketteki müşteri ve/veya ürünlere yönelik ilişkili komisyon hesaplama ayarlarında belirlenen şekilde çalışanın komsiyon payı temel alınarak belirlenir.




