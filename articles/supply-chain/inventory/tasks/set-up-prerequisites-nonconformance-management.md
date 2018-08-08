---
title: "Yönetim ön koşullarını ayarlama"
description: "Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu yordamı kullanın."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: tr-tr
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Yönetim ön koşullarını ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu yordamı kullanın. Uyumsuzluk, açıklayıcı bilgilerin sorunun kaynağını ve tipini içerdiği bir kalite sorunu olan bir yordamı veya maddeyi tanımlar. Bu yordam, USMF demo verisi şirketini kullanır. Bu yordam genellikle kalite yöneticisi tarafından gerçekleştirilir.


## <a name="enable-quality-management-processes-within-the-company"></a>Şirket içindeki kalite yönetimi işlemlerini etkinleştirin
1. Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.
2. Kalite yönetimi sekmesine tıklayın.
3. Kalite yönetimi kullan alanında Evet'i seçin.
    * Şirket için kalite yönetimi işlemlerini etkinleştirmek için bu parametreyi seçin.  
4. Saatlik ücret alanına bir numara girin.
    * Yerel para biriminde saatlik ücret girmek için Saatlik ücret alanını kullanın. Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetleri hesaplamak için kullanılır. Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar ve diğer işlevlerle etkileşime girmez.  
5. Rapor kurulumu'na tıklayın.
    * Bu sayfa, farklı türde kalite yönetimi raporlarında kullanılacak kalite raporu not türlerini tanımlamanıza olanak sağlar.  
6. Sayfayı kapatın.
7. Sayfayı kapatın.

## <a name="enable-user-for-nonconformance-processing"></a>Kullanıcıyı uygunsuzluk işleme için etkinleştirin.
1. Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.
    * Bir uygunsuzluk onayını işlemek için uygunsuzlukları onaylayan veya reddeden kullanıcının atanmış kullanıcılar sayfasında bir "Ad" değeri olmalıdır. Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.  
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, 'Ricardo' değerini girerek filtreleme yapın.
    * Onaylama veya reddetme işlemlerini yapacak kullanıcıyı bulmak için uygunsuzluk kayıtlarında filtre kullanın.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Bir uygunsuzluk onayını işlemek için uygunsuzlukları onaylayan veya reddeden kullanıcının, Kullanıcılar sayfasında atanmış bir "Ad" değeri olduğundan emin olun.  
4. Kullanıcı seçenekleri'ni tıklatın.
5. Tercihler sekmesini tıklatın.
6. Belge işlemeyi etkinleştir alanında Evet'i seçin.
    * Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.  
7. Sayfayı kapatın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Uygunsuzluk işleme için tanı türlerini tanımlayın
1. Stok yönetimi > Kurulum > Kalite yönetimi > Tanı türleri öğesine gidin.
    * Tanılama işlemleri için bir sınıflandırma tanımlamak için Tanılama türleri sayfasını kullanın. Bir düzeltme, onaylanan bir uyumsuzluk için yapılması gereken tanı eyleminin tipini, bunu gerçekleştirecek kişiyi ve istenen ve planlanan tamamlama tarihini tanımlar.  
2. Yeni'ye tıklayın.
3. Tanı alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Sayfayı kapatın.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Uygunsuzluk işleme için kalite giderlerini tanımlayın
1. Stok yönetimi > Kurulum > Kalite yönetimi > Kalite giderleri öğesine gidin.
    * Kalite giderleri sayfasını, uygunsuzluklar ile ilgili işlemlerinde kullanılacak giderlerin sınıflandırılmasını tanımlamak için kullanın.  
2. Yeni'ye tıklayın.
3. Masraf kodu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Sayfayı kapatın.

## <a name="define-the-operations-for-nonconformance-processing"></a>Uygunsuzluk işleme için operasyonları tanımlayın
1. Stok yönetimi > Kurulum > Kalite yönetimi > Operasyonlar öğesine gidin.
    * Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için Operasyonlar sayfasını kullanın. Uyumsuzluğa ilgili bir operasyonu ilişkilendirdiğinizde, operasyonu gerçekleştirmek için gereken ilgili malzemeler, emek saatleri ve tahmini maliyetlerle ilgili ayrıntılı bilgiler tanımlayabilirsiniz. Bu bilgiler, operasyonu gerçekleştirmek için gereken tahmini maliyetin hesaplanmasında bir temel sağlar.  
2. Yeni'ye tıklayın.
3. Operasyon alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Sayfayı kapatın.

## <a name="define-problem-types-for-nonconformance-processing"></a>Uygunsuzluk işleme için problem türlerini tanımlayın
1. Stok yönetimi > Kurulum > Kalite yönetimi > Problem türleri öğesine gidin.
    * Çeşitli uygunsuzluk türlerinde karşılaşılan kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için Sorun türleri sayfasını kullanın. Uygunsuzluk türlerine; Dahili, Müşteri, Satıcı, Hizmet talebi, Üretim ve Eş ürün üretimi gibi türler dahildir. Tek bir sorun türü birden çok uygunsuzluk türüyle ilişkilendirilebilir.  
2. Yeni'ye tıklayın.
3. Problem türü alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Uyumsuzluk tipleri'ne tıklayın.
    * Bir sorun türünün bir veya birden fazla uygunsuzluk türünde kullanmak üzere yetkilendirmek için Uygunsuzluk türleri sayfasını kullanın. Örneğin, bir kusur koduyla ilgili bir sorun tipi tüm uyumsuzluk tipleri için geçerli olurken, müşteri şikayetleri hakkındaki bir sorun tipi yalnızca müşteri ve servis isteği uyumsuzluk tipleri için geçerli olabilir.  
6. Yeni'ye tıklayın.
7. Listede, seçili satırı işaretleyin.
8. Uygunsuzluk türü alanında, bir seçenek seçin.
9. Sayfayı kapatın.
10. Sayfayı kapatın.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Uygunsuzluk işleme için karantina bölgelerini tanımlayın
1. Stok yönetimi > Kurulum > Kalite yönetimi > Karantina bölgeleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Karantina bölgesi alanında bir değer girin.
4. Açıklama alanına bir değer girin.
5. Sayfayı kapatın.

