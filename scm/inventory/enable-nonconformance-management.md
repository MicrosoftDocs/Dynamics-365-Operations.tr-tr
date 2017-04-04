---
title: "Nonconformance Yönetimi"
description: "Bu makalede, uygunsuzlukları kullanmak için gereken temel kurulum açıklanmaktadır. Kalite emirleri kullanmak istiyorsanız ek kurulum gereklidir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 6f25e2930ff265df1f938cdf56e8a0f4993617af
ms.lasthandoff: 03/31/2017


---

# <a name="nonconformance-management"></a>Nonconformance Yönetimi

Bu makalede, uygunsuzlukları kullanmak için gereken temel kurulum açıklanmaktadır. Kalite emirleri kullanmak istiyorsanız ek kurulum gereklidir. 

Uygunsuzluk yönetimini etkinleştirmek için şu adımları izleyin:

1.  Uygunsuzlukla bağlantılı olan Envanter ve depo yönetimi parametrelerini tanımlayın:
    -   **Kalite yönetimini kullan** seçeneğini **Evet** konumuna ayarlayın.
    -   **Saatlik ücret** alanına saatlik işçilik ücretini yerel para birimi cinsinden girin. Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetlerin hesaplanmasında kullanılır. Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar. Diğer işlevlerle bir etkileşimi yoktur.
    -   Kullanım **Kalite Yönetimi** üzerinde sekme **rapor Kurulumu** sayfa yazdırmak için belgenin türünü tanımlamak için. Nonconformance raporu, nonconformance etiket veya düzeltme raporu yazdırabilirsiniz. Bir raporda farklı belge türlerini yazdırmak veya dahili ve harici notları yazdırmak için birden fazla kayıt tanımlayabilirsiniz. Uygunsuzluk ve düzeltmeler için ayrı ayrı benzersiz belge türleri tanımlamak için **Belge türü** sayfasını kullanabilirsiniz. Örneğin, benzersiz uygunsuzluk belge türünü kullanarak bir uygunsuzluk hakkında notlar girmek için istiyorsunuz. Bu durumda, benzersiz belge türünü rapor seçeneklerinde belirleyin.
    -   Uygunsuzluk ve düzeltme referansları için numara serilerini etkinleştirin.

2.  Uygunsuzluğun kullanıcı tarafından onaylanmasını etkinleştirin. Bir uygunsuzluğu onaylaması gereken her bir kullanıcıya bir personel atamak için **Kullanıcılar** sayfasındaki **Ad** alanını kullanın. Sistem, uygunsuzluk geçmişini izlemek için bir uygunsuzluk durumunu değiştiren personeli kullanır. Kullanıcılar bir personel tanımlayıcı atanmadığı sürece bir uygunsuzluğu onaylayamazlar.
3.  Uygunsuzluk olarak atanacak sorun türlerini tanımlayın. Çeşitli uygunsuzluk türleri için karşılaşılan kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için **Sorun türleri** sayfasını kullanın. Şu uygunsuzluk türlerini ayarlayabilirsiniz: **Dahili**, **Müşteri**, **Satıcı**, **Hizmet talebi**, **Üretim** ve **Eş ürün üretimi**. Bir sorun türünün bir veya birden fazla uygunsuzluk türünde kullanılmasını yetkilendirmek için **Uygunsuzluk türleri** sayfasını kullanın. Örneğin, bir kusur koduyla ilgili bir sorun türü tüm uygunsuzluk türleri için geçerli olabilirken, müşteri şikayetleriyle ilgili bir sorun türü yalnızca **Müşteri** ve **Hizmet talebi** uygunsuzluk türleri için geçerli olabilir.
4.  Kusurlu malzemelerin nasıl işlenmesi gerektiği hakkında kılavuz sağlamak için karantina bölgelerini tanımlayın. Bir uygunsuzluğa atanabilecek bölgeleri tanımlamak için **Karantina bölgeleri** sayfasını kullanın. Yazdırılan uygunsuzluk etiketi, kusurlu malzemelerin nasıl işlenmesi gerektiği hakkında kılavuz sağlamak için, atanan karantina bölgesini ve kullanım hakkında bilgiler içerir. Bölgeler envanter konumlarına veya operasyon kaynaklarına karşılık gelebilir.
5.  Düzeltmelere atanacak tanılama türerini tanımlayın. Tanılama işlemleri için bir sınıflandırma tanımlamak için **Tanılama türleri** sayfasını kullanın. Bir düzeltme, onaylanan bir uyumsuzluk için hangi türde tanılama işleminin yürütülmesi ve bu işlemin kimin tarafından gerçekleştirilmesi gerektiğini tanımlar. Ayrıca, istenen tamamlanma tarihi ve planlanan tamamlanma tarihini belirtir.
6.  Uygunsuzluğa atanacak ilgili operasyonları tanımlayın. Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için **Operasyonlar** sayfasını kullanın. Bir uyumsuzluğa ilgili bir operasyon atadığınızda, operasyonu gerçekleştirmek için gereken ilgili malzemeler hakkında bilgiler, işçilik saatleri ve çeşitli ücretler vb. gibi ayrıntılı bilgiler sağlayabilirsiniz. Bu bilgiler, operasyon için tahmini maliyetini hesaplanmasında kullanılır. Ayrıntılı bilgiler ve tahmini maliyetler bilgi amaçlıdır. Kalite için ilgili operasyonlar, bir üretim rotası için tanımlanabilecek operasyonlardan farklıdır.


<a name="see-also"></a>Ayrıca bkz.
--------

[Oluşturma ve işleme uyumsuzluğu (görev Kılavuzu)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Quality management processes](quality-management-processes.md)

[Uyumsuzluk Yönetimi (görev Kılavuzu) için önkoşulları ayarlayın](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)


