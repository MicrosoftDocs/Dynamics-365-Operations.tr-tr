---
title: Konteyner kullanımını ayarlama
description: Bu konu, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b5ad1bdd91a2fb9109f29400f082e9a8af009ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216954"
---
# <a name="set-up-containerization"></a>Konteyner kullanımını ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar. Otomatik konteyner kullanımı, bir dalga işlendiğinde sevkiyatlar için konteynerleri ve çekme işini oluşturur ve iş satırları, konteynerlere sığacak miktarlara bölünür. Bu, ambar çalışanlarına, maddeleri doğrudan seçilen konteynere çekmelerine yardımcı olur. El ile yapılan paketleme işlemi ile karşılaştırıldığında, örneğin konteynerler oluşturma, maddeler atama ve konteyner kapanışı gibi işlemler, sistem tarafından otomatikleştirilir. Bu yordam, USMF demo şirketin kullanır ve Ambar Yöneticisi tarafından gerçekleştirilir.


## <a name="set-up-a-wave-template"></a>Dalga şablonu ayarlama
1. Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları**'na gidin.
2. **Yeni**'yi seçin.
3. **Dalga şablonu adı** alanına bir değer girin.
4. **Dalga şablonu açıklaması** alanında bir değer girin.
5. **Tesis** alanına bir değer girin veya buradan bir değer seçin.
6. **Ambar** alanında bir değer girin veya bir değer seçin.
7. **Yöntemler** bölümünü genişletin. **Seçili yöntemler** bölmesi, seçili dalga şablon türü için yöntemleri listeler. Dalga şablonu, konteynerli yöntemi içermelidir.  
8. **Dalga adımı kodu** alanına bir değer girin. Eklenen yöntem için herhangi bir kod olabilecek Dalga adım kodu girin. Yöntemi birden çok kez eklemek ve farklı dalga adım kodları atamak da mümkündür. Bunu yapmak için bu yöntemin **Dalga işlem yöntemleri** sayfasında **Tekrar edilebilir**'i seçin.  
9. **Kaydet**'i seçin.
10. Sayfayı kapatın.

## <a name="set-up-a-container-type"></a>Konteyner türü ayarlama
1. Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri**'ne gidin. **Konteyner türleri** sayfasında, konteynerlerinizi tanımlayabilirsiniz. Konteynerlerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve yükseklik dahil olmak üzere yapılandırabilirsiniz. Bu örnekte, üç farklı boyutta kutulara sahibiz.  
2. **Yeni**'yi seçin.
3. **Konteyner türü kodu** alanına bir değer girin.
4. **Dara ağırlığı** alanına bir sayı girin.
5. **Maksimum ağırlık** alanında bir sayı girin.
6. **Hacim** alanına bir sayı girin.
7. **Uzunluk** alanına bir sayı girin.
8. **Genişlik** alanına bir sayı girin.
9. **Yükseklik** alanına bir sayı girin.
10. **Tanım** alanına bir değer girin.
11. **Kaydet**'i seçin.
13. Üç toplam konteyner türü yapmak için iki kez daha 2-11 adımları yineleyin.
14. Sayfayı kapatın.

## <a name="set-up-a-container-group"></a>Bir konteyner grubu ayarla
1. Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > Konteynerler > Konteyner grupları**'na gidin.
2. Eylem bölmesinde, **Yeni**'yi seçin. Konteyner türleri için mantıksal grupları ayarlayabilirsiniz. Her bir grup için, konteynerlerin paketleneceği sıralamayı ve konteynerlerin doldurulacağı yüzdeyi belirtebilirsiniz. Maddenin ebat boyutları, bir konteynere sığı sığmayacağını belirlemekte kullanılır. Maddenin ebat boyutuna en yakın olan konteyner kullanılacaktır. Bir grup içinde birden çok konteyner türü varsa, sırayı boyuta göre düzenlemenizi öneririz, böylelikle en büyük konteyner birinci, sıralama içerisinde birinci numarada olur ve en küçük konteyner en sona kalır.    
3. **Konteyner grup kimliği** alanında, daha önce oluşturduğunuz bir değer yazın.
4. **Tanım alanına** bir değer girin.
5. 2-4 adımları, daha önce oluşturduğunuz tüm üç konteyner türleri için yineleyin.
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.

## <a name="set-up-a-container-build-template"></a>Bir konteyner yapılandırma şablonu
1. Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > Konteynerler > Konteyner derleme şablonu**'na gidin.
2. **Yeni**'yi seçin. Konteyner yapılandırma şablonu, hangi konteyner kullanım işleminin gerçekleştirildiğine dayalıdır. Her bir konteyner yapılandırma şablonu, bir dalga şablonu tarafından kullanılacak bir konteyner kullanım işlemini tanımlar. **Sorguyu düzenle** seçeneği, seçili şablonun işleneceği koşulları tanımlamanızı sağlar. Örneğin, yalnızca belirli müşteriler, ürünler veya ambarlar için konteyner kullanmayı çalıştırmak isteyebilirsiniz veya karşılık gelen sorgu aralıklarını şablona ekleyebilirsiniz. **Dalga adım kodu** alanı, konteyner yapılandırma şablonunun dalga şablonundaki adımlara nasıl bağlandığını gösteren alandır. Bir dalga yürütüldüğünde hangi kapsayıcı yapı şablonunun konteyner kullanımını başlatmak için kullanılacağını belirler. Taban sorgu türü alanı, neyin paketleneceğini ve filtre sorgusunun neye dayandırılacağını belirler. 
3. **Konteyner şablonu kimliği** alanında bir değer girin.
4. **Konteyner grup kimliği** alanında bir değer girin veya bir değer seçin.
5. **Dalga adımı kodu** alanına bir değer girin.
6. **Bölünmüş çekmelere izin ver** onay kutusunu işaretleyin.
7. **Kaydet**'i seçin.
8. **Konteyner karıştırma sınırlamalarına** tıklayın. Mantık bölümlerini karıştırmak, konteynerler içindeki paketleme tahsisat satırları için kurallar eklemenize olanak sağlar. Örneğin, maddeler konteynerlere atandığında **Madde numarası alanını** eklerseniz, yeni bir madde numarası olduğunda, yeni bir konteyner oluşturulur. Bu, çalışanların aynı konteyner içerisindeki iki farklı müşteri için tahsisat satırlarını paketlemelerinin önüne geçer.  
9. **Yeni**'yi seçin.
10. **Tablo** alanında, bir seçenek seçin.
11. **Alan Seç** alanına bir değer girin veya buradan bir değer seçin.
12. **Tamam**'ı seçin.

