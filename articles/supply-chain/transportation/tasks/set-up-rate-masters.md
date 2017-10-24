--- 
title: "Ana oranları ayarlama"
description: "Bu yordam, bir ana oran kurmayı göstermektedir."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a>Ana oranları ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir ana oran kurmayı göstermektedir. Genellikle Lojistik Yöneticisi, taşıyıcılar ile imzalanmış olan sözleşmelere bağlı olarak ana oranları ayarlar. Bu senaryoda bir hava taşıyıcısı için ana oran ayarlayacaksınız. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-rate-master"></a>Ana oranı ayarlayın
1. Taşıma yönetimi > Kurulum > Derecelendirme > Ana oran öğesine gidin.
2. Yeni'ye tıklayın.
3. Ana oran alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Oran meta veri kimliği alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu oran asıl kullanarak TMS altyapısı tarafından beklenen meta verileri tanımlar gibi kuru master için gerekli veri derecelendirme meta veriler kimliği belirleyecektir.  
6. Bu örnekte, P2P seçeneğini seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Kaydet'e tıklayın.

## <a name="set-up-rate-base"></a>Oran tabanını ayarla
1. Taban türü oranı'na tıklayın.
    * Taban oranı, taşıyıcının oranını belirler ve gümrük tarifesi yapısı oluşturmada, kesme kalıplarında belirtilen kesme noktalarındaki oranları yapılandırdığı için kullanılabilir.  
2. Yeni'ye tıklayın.
3. Taban türü oranı alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Ana mola alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır. Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.  
6. Bu örnek için ağırlık kullanın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Ayrıntılar bölümünün genişletilmiş görünümüne geçin.
9. Yeni'yi tıklatın.
10. Teslim posta kodu kaynağı alanında, '30301' yazın.
11. Giden posta kodu bırakma alanında, '30318' yazın.
12. Teslimat ülkesi bölgesi alanına 'ABD' yazın.
13. <1,00 Lbs alanında '100' yazın.
    * Yükün toplam ağırlığı 1 libreden az ise lbs başına ücret girin.  
14. < 5,00 Lbs alanında, '300' yazın.
    * Yükün toplam ağırlığı 5 libreden az ise lbs başına ücret girin.  
15. < 20,00 Lbs alanında, '500' yazın.
    * Yükün toplam ağırlığı 20 libreden az ise lbs başına ücret girin.  
16. < 100,00 Lbs alanında, '1000' yazın.
    * Yükün toplam ağırlığı 100 libreden az ise lbs başına ücret girin.  
17. < 1.000,00 Lbs alanında, '3000' yazın.
    * Yükün toplam ağırlığı 1000 libreden az ise lbs başına ücret girin.  
18. Kaydet'e tıklayın.
19. Sayfayı kapatın.

## <a name="assign-rate-base"></a>Oran tabanı atama
1. Taban oranı atamaları bölümünün genişletilmiş görünümüne geçin.
2. Yeni'ye tıklayın.
    * Her ana oran için birden fazla oran tabanı atamanız olabilir. Bu hedeflere, hizmetlere veya farklı taba oranlarına bağlı olarak her taşıyıcı için birkaç farklı fiyat noktaları oluşturmaya olanak sağlar. Bu yordamda sadece bir oranı tabanı ataması oluşturacaksınız.  
3. İsim alanına bir değer yazın.
4. Taban oranı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Hizmet alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Çekme posta kodu alanına '98052' yazın.
    * Bu oran tabanı atamasının hangi posta kodundan itibaren geçerli olacağını belirtin.    
10. Çekme Ülke Bölge alanında 'USA' yazın.
11. Kaydet'e tıklayın.


