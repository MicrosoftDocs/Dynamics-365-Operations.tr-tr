---
title: İş yükü kapasitesini zamanlama
description: Bu konuda, bir ambardaki çalışanlar veya tüm ambar için iş yükü kapasitesinin nasıl ayarlanacağı ve zamanlanacağı açıklanmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8db243949b2aeee0a8263276234d439652905449
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965589"
---
# <a name="schedule-workload-capacity"></a>İş yükü kapasitesini zamanlama

[!include[banner](../includes/banner.md)]

Ambarlar için iş yükü kapasitesini zamanlayabilir ve ayrı ambarlardaki çalışanlar için mevcut ve gelecekteki iş yüklerini yansıtabilirsiniz. Tüm ambar için iş yükünü veya gelen ve giden iş yükleri için iş yükünü ayrı olarak yansıtabilirsiniz.

Seçili ambarlar için proje iş yükü çıktısını yansıtmak için master planlama verileri bu ambarlar için kullanılabilir olmalıdır. Daha fazla bilgi için bkz. [Master planlara genel bakış](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Bir ambar için iş yüklerini zamanlama ve görüntüleme

Bir ambar için iş yükü kapasitesini zamanlamak üzere bir veya daha fazla ambar için bir iş yükü kurulumu oluşturun ve ardından iş yükü kurulumu bir master plan ile ilişkilendirin. İş yükü kapasitesi kurulumunda, gelen ve giden hareketler için ağırlık veya hacim sınırları tanımlayabilirsiniz. Her ambar için birden fazla kurulum oluşturabilir ve ardından kurulumu ayrı master planlarla ilişkilendirebilirsiniz. Örneğin, işgücündeki dönemsel değişikliklere uyum sağlamak için bu yöntemi kullanabilirsiniz.

Bir ambar için çalışanlar hem gelen hem de giden iş yükü hareketleriyle çalışıyorsa, ambar kapasitesi kurulumunu iş yükü birleştirilmiş görünümde yansıtılacak şekilde yapılandırabilirsiniz.

Ambarlar için iş yüklerini zamanlamak ve görüntülemek için aşağıdaki görevleri tamamlamalısınız:

1. Bir iş yükü kapasitesi kurulumu oluşturun ve bir veya daha fazla ambar için iş yükü kapasite sınırlarını tanımlayın.
2. İş yükü tahminleri oluşturmak için kapasite iş yükü kurulumunu master plan ile ilişkilendirin ve bu tahminlerin ne kadar süreyle uygulanacağını belirtin.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Bir ambar için bir iş yükü kapasite kurulumu oluşturma

1. **Stok yönetimi** \> **Kurulum** \> **Ambar izleme** \> **Kapasite iş yükü**'nü seçin.
2. Eylem bölmesinde, iş yükü kapasite kurulumu oluşturmak için **Yeni**'yi seçin.
3. **Ambarlar** hızlı sekmesinde **Yeni**'yi seçin ve bir ambarı iş yükü kapasite kurulumuyla ilişkilendirmek için satırdaki değerleri girin.
4. **Kapasite iş yükü** raporunun gelen ve giden hareketler için toplam iş yükünü tek bir görünümde göstermesi gerekiyorsa **Birleştirilmiş gelen ve giden iş yükü** onay kutusunu seçin.
5. **Hareket türleri** hızlı sekmesinde iş yükü sınırlarının uygulanacağı gelen ve giden hareket türlerini seçin.

    > [!NOTE]
    > Hem gelen iş yükü hem de giden iş yükü için en az bir hareket türü seçmeniz gerekir.

#### <a name="define-limits-for-volume-or-weight"></a>Hacim veya ağırlık için sınırları tanımlama

Ambar iş gücü için ilgili sınırlamaya bağlı olarak, hacim veya ağırlık sınırları ayarlayabilirsiniz. Belirttiğiniz sınırlar **İş yükü kapasite** raporunda görebileceğiniz iş gücü kapasite yansıtmasına dahil edilir.

Maddeler için hacim ve ağırlıkla ilgili bilgileri yansıtmak için, tüm ürünler için bir stok maddesinin standart hacmi ve bir stok maddesinin ağırlığı belirtilmelidir. Gerekli alanlar aşağıdaki **Serbest bırakılan ürün ayrıntıları** sayfasının **Stok yönetimi** hızlı sekmesindeki alan gruplarında bulunur:

- İşleme
- Fiziksel boyutlar
- Ağırlık ölçümleri

Bu bilgiler doğru bir şekilde belirtilmezse, **İŞ yükü kapasite** raporu oluşturduğunuzda bir ileti alırsınız. Rapordan, daha sonra gelecekteki iş yükünü yansıtmak için gereken eksik bilgileri tanımlamak üzere ayrıntıya girebilirsiniz.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Bir iş yükü kapasite kurulumunu bir master plan ile ilişkilendirme

1. **Stok Yönetimi** \> **Periyodik** \> **İş yükünü zamanla**'yı seçin.
2. **Master plan** alanında, iş yükü tahminleri için kullanılacak master planı seçin.
3. **Gün sayısı** alanında, iş yükü tahmininin kapsadığı gün sayısını belirtin.
4. **iş yükü** alanında, master plan ile ilişkilendirilecek iş yükü kurulumu seçin.

### <a name="view-workload-capacity"></a>İş yükü kapasitesini görüntüleme

1. **Stok Yönetimi** \> **Sorgular ve raporlar** \> **Fiziksel stok raporları** \> **İş yükü kapasitesi**'ni seçin.
2. **Sütun sayısı** alanında, raporda gösterilecek sütun sayısını belirtin.
3. **Sipariş türü** alanında raporda yansıtılacak siparişlerin türünü belirtmek için **Planlandı ve onaylandı**, **Planlandı** veya **Onaylandı**'yı seçin.
4. **Yük türü** alanında, iş yükü kapasitesinin hacim veya ağırlık için mi yansıtılacağını belirtmek üzere bir yük türü seçin.
5. **İş yükü kapasitesi** alanında bir iş yükü kapasitesi kurulumu seçin.
