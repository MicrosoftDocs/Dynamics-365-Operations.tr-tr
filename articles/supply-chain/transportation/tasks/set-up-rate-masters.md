---
title: Ana oranları ayarlama
description: Bu yordam, bir ana oran kurmayı göstermektedir.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809002"
---
# <a name="set-up-rate-masters"></a>Ana oranları ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ana oran kurmayı göstermektedir. Genellikle Lojistik Yöneticisi, taşıyıcılar ile imzalanmış olan sözleşmelere bağlı olarak ana oranları ayarlar. Bu senaryoda bir hava taşıyıcısı için ana oran ayarlayacaksınız. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.

## <a name="set-up-break-master"></a>Ana kırılımı ayarlama

1. **Taşıma yönetimi > Kurulum > Derecelendirme > Ana kırılım** öğesine gidin. Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır. Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.  
1. **Yeni**'yi seçin.
1. **Ana kırılım** alanına bir değer girin.
1. **Ad** alanına bir değer girin.
1. **Veri türü** alanında bir veri türü seçin.
1. **Karşılaştırma** alanına, istenen karşılaştırma türünü (işleçler kullanarak) girin.
1. **Kırılım birimi** alanında, kırılım birimini girin.
1. **Ayrıntılar** bölümünde, fiyatlandırma yapısı için gerektiği kadar kırılım oluşturun.
1. **Kaydet**'i seçin.

## <a name="set-up-rate-master"></a>Ana oranı ayarlayın

1. **Taşıma yönetimi > Kurulum > Derecelendirme > Ana oran** öğesine gidin.
1. **Yeni**'yi seçin.
1. **Ana oran** alanına bir değer yazın.
1. **Ad** alanına bir değer yazın.
1. **Değerlendirme meta veri kimliği** alanında, aramayı açmak için açılır menü düğmesini seçin. Bu oran asıl kullanarak taşıma yönetimi altyapısı tarafından beklenen meta verileri tanımlar gibi kuru master için gerekli veri derecelendirme meta veriler kimliği belirleyecektir.  
1. Bu örnekte, P2P seçeneğini seçin. Bu, demo verilerinde zaten tanımlanmıştır.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Kaydet**'i seçin.

## <a name="set-up-rate-base"></a>Oran tabanını ayarla

1. **Oran tabanı**'nı seçin.
    * Taban oranı, taşıyıcının oranını belirler ve gümrük tarifesi yapısı oluşturmada, kesme kalıplarında belirtilen kesme noktalarındaki oranları yapılandırdığı için kullanılabilir.  
2. **Yeni**'yi seçin.
3. **Oran tabanı** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Ana kırılım** alanında, aramayı açmak için açılır menü düğmesini seçin.
    * Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır. Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.  
6. Bu örnek için ağırlık değerini kullanın. Bu, demo verilerinde zaten tanımlanmıştır.
7. Listeden, vurgulanan satırdaki bağlantıyı seçin.
8. **Ayrıntılar** bölümünü genişletin.
9. **Yeni**'yi seçin.
10. **Teslimat Posta Kodu Kaynağı** alanına, "30301" yazın.
11. **Teslimat Posta Kodu Hedefi** alanına, "30318" yazın.
12. **Teslimat ülkesi bölgesi** alanına "ABD" yazın.
13. **<1,00 Lbs** alanına "100" yazın.
    * Yükün toplam ağırlığı 1 libreden az ise lbs başına ücret girin.  
14. **<5,00 Lbs** alanına "300" yazın.
    * Yükün toplam ağırlığı 5 libreden az ise lbs başına ücret girin.  
15. **<20,00 Lbs** alanına "500" yazın.
    * Yükün toplam ağırlığı 20 libreden az ise lbs başına ücret girin.  
16. **<100,00 Lbs** alanına "1000" yazın.
    * Yükün toplam ağırlığı 100 libreden az ise lbs başına ücret girin.  
17. **<1.000,00 Lbs** alanına "3000" yazın.
    * Yükün toplam ağırlığı 1000 libreden az ise lbs başına ücret girin.  
18. **Kaydet**'i seçin.
19. Sayfayı kapatın.

## <a name="assign-rate-base"></a>Oran tabanı atama

1. **Oran tabanı atamaları** bölümünü genişletin.
2. **Yeni**'yi seçin.
    * Her ana oran için birden fazla oran tabanı atamanız olabilir. Bu hedeflere, hizmetlere veya farklı taba oranlarına bağlı olarak her taşıyıcı için birkaç farklı fiyat noktaları oluşturmaya olanak sağlar. Bu yordamda sadece bir oranı tabanı ataması oluşturacaksınız.  
3. **Ad** alanına bir değer yazın.
4. **Oran tabanı** alanında, aramayı açmak için açılır menü düğmesini seçin.
5. Listeden, vurgulanan satırdaki bağlantıyı seçin.
6. **Servis** alanında, aramayı açmak için açılır menü düğmesini seçin.
7. Listede, istenen kaydı bulun ve seçin.
8. Listeden, vurgulanan satırdaki bağlantıyı seçin.
9. **Çekme Posta Kodu** alanına "98052" yazın.
    * Bu oran tabanı atamasının hangi posta kodundan itibaren geçerli olacağını belirtin.
10. **Çekme Ülke Bölgesi** alanında "ABD" yazın.
11. **Kaydet**'i seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]