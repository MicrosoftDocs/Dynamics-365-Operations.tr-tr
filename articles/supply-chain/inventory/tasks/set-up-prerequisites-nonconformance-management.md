---
title: Uyumlu olmayan yönetim için ön şartları ayarlama
description: Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu konuyu kullanın.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961535"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Uyumlu olmayan yönetim için ön şartları ayarlama

[!include [banner](../../includes/banner.md)]

Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu konuyu kullanın. Uyumsuzluk, açıklayıcı bilgilerin sorunun kaynağını ve tipini içerdiği bir kalite sorunu olan bir yordamı veya maddeyi tanımlar. Bu yordam, USMF demo verisi şirketini kullanır. Bu yordam genellikle kalite yöneticisi tarafından gerçekleştirilir.


## <a name="enable-quality-management-processes-within-the-company"></a>Şirket içindeki kalite yönetimi işlemlerini etkinleştirin
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.
2. **Kalite yönetimi** sekmesini seçin.
3. Şirket için kalite yönetimi süreçlerini etkinleştirmek için **Kalite yönetimi kullan**  alanında **Evet**'i seçin. 
4. **Saatlik ücret** alanına yerel para birimi cinsinden bir sayı girin. Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetleri hesaplamak için kullanılır. Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar ve diğer işlevlerle etkileşime girmez.  
5. Farklı türde kalite yönetimi raporlarında kullanılacak kalite raporu not türlerini tanımlamak için **Rapor kurulumu**'nu seçin.

## <a name="enable-user-for-nonconformance-processing"></a>Kullanıcıyı uygunsuzluk işleme için etkinleştirin.
1. Gezinti bölmesinde **Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin. 
2. Onaylama veya reddetme işlemlerini yapacak kullanıcıyı bulmak için uygunsuzluk kayıtlarında Hızlı Filtreleme kullanın. Örneğin, **Ad** alanında `Ricardo` değerini girerek filtreleme yapın. Bir uygunsuzluk onayını işlemek için uygunsuzlukları onaylayan veya reddeden kullanıcının **Kullanıcılar** sayfasında atanmış bir "Ad" değeri olmalıdır. Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.  
3. İstenen kaydın satırını işaretleyin.
4. **Kıllanıcı seçenekleri**'ni seçin.
5. **Tercihler** sekmesini seçin.
6. **Belge işlemeyi etkinleştir** alanında **Evet**'i seçin.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Uygunsuzluk işleme için tanı türlerini tanımlayın
1. Gezinti bölmesinde **Modüller > Stok yönetimi > Kurulum > Kalite yönetimi > Tanı türleri** öğesine gidin. Tanılama işlemleri için bir sınıflandırma tanımlamak için **Tanılama türleri** sayfasını kullanın. Bir düzeltme, onaylanan bir uyumsuzluk için yapılması gereken tanı eyleminin tipini, bunu gerçekleştirecek kişiyi ve istenen ve planlanan tamamlama tarihini tanımlar.  
2. **Yeni**'yi seçin.
3. **Tanı** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Uygunsuzluk işleme için kalite giderlerini tanımlayın
1. Gezinti bölmesinde **Modüller > Stok yönetimi > Kurulum > Kalite yönetimi > Kalite giderleri** öğesine gidin. **Kalite giderleri** sayfasını, uygunsuzluklar ile ilgili işlemlerinde kullanılacak giderlerin sınıflandırılmasını tanımlamak için kullanın.  
2. **Yeni**'yi seçin.
3. **Masraf kodu** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.

## <a name="define-the-operations-for-nonconformance-processing"></a>Uygunsuzluk işleme için operasyonları tanımlayın
1. Gezinti bölmesinde **Modüller > Stok yönetimi > Kurulum > Kalite yönetimi > Operasyonlar** öğesine gidin. Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için **Operasyonlar** sayfasını kullanın. Uyumsuzluğa ilgili bir operasyonu ilişkilendirdiğinizde, operasyonu gerçekleştirmek için gereken ilgili malzemeler, emek saatleri ve tahmini maliyetlerle ilgili ayrıntılı bilgiler tanımlayabilirsiniz. Bu bilgiler, operasyonu gerçekleştirmek için gereken tahmini maliyetin hesaplanmasında bir temel sağlar.  
2. **Yeni**'yi seçin.
3. **Operasyon** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.

## <a name="define-problem-types-for-nonconformance-processing"></a>Uygunsuzluk işleme için problem türlerini tanımlayın
1. Gezinti bölmesinde **Modüller > Stok yönetimi > Kurulum > Kalite yönetimi > Sorun türleri** öğesine gidin. Çeşitli uygunsuzluk türlerinde karşılaşılan kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için **Sorun türleri** sayfasını kullanın. Uygunsuzluk türlerine **Dahili**, **Müşteri**, **Satıcı**, **Hizmet talebi**, **Üretim** ve **Eş ürün üretimi** gibi türler dahildir. Tek bir sorun türü birden çok uygunsuzluk türüyle ilişkilendirilebilir.  
2. **Yeni**'yi seçin.
3. **Problem türü** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Uygunsuzluk türleri**'ni seçin. Bir sorun türünün bir veya birden fazla uygunsuzluk türünde kullanmak üzere yetkilendirmek için **Uygunsuzluk türleri** sayfasını kullanın. Örneğin, bir kusur koduyla ilgili bir sorun tipi tüm uyumsuzluk tipleri için geçerli olurken, müşteri şikayetleri hakkındaki bir sorun tipi yalnızca müşteri ve servis isteği uyumsuzluk tipleri için geçerli olabilir.  
6. **Yeni**'yi seçin.
7. Yeni satırın **Uygunsuzluk türü** alanında, bir seçenek seçin.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Uygunsuzluk işleme için karantina bölgelerini tanımlayın
1. Gezinti bölmesinde **Modüller > Stok yönetimi > Kurulum > Kalite yönetimi > Karantina bölgeleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Karantina bölgesi** alanında bir değer girin.
4. **Tanım** alanına bir değer girin.
5. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]