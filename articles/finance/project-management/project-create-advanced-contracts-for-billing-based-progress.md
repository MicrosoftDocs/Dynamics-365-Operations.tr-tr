---
title: İlerlemeye göre faturalama için gelişmiş sözleşmeler oluşturma
description: Bu konu, tamamlanan çalışmanın yüzdesine göre müşteriler için fatura oluşturabilmek amacıyla proje sözleşmelerinin nasıl oluşturulacağını açıklar.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282853"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>İlerlemeye göre faturalama için gelişmiş sözleşmeler oluşturma
[!include [banner](../includes/banner.md)]

Bu konu, tamamlanan çalışmanın yüzdesine göre müşteriler için fatura oluşturabilmek amacıyla proje sözleşmelerinin nasıl oluşturulacağını açıklar. Fatura tutarları, proje için ayarladığınız çalışmanın bütçe kategorileri için otomatik olarak hesaplanır. Fatura zamanlaması, müşteriyle proje sözleşmesini görüşmeniz sırasında ayarlanır.

Bu konudaki yordamları bir sözleşme, ilişkili proje ve proje için ayarladığınız çalışmanın bütçe kategorileri için fatura tutarlarını hesaplamakta kullanılan faturalama kurallarını ayarlamak için kullanın.

Sözleşmeyi ve projeyi oluşturduktan sonra, projenin ayrıntılarını ayarlayabilirsiniz. Örneğin, faaliyetleri tanımlayabilir ve projeye çalışan atayabilirsiniz.

## <a name="example"></a>Örnek

Kuruluşunuz bir yazılım geliştirme firması. Bir müşteri için, 20.000 ABD Doları (USD) toplam ücret karşılığında bir muhasebe bordro paketi geliştirmeyi kabul ediyorsunuz. Kuruluşunuz, projenin belirli yüzdelerini tamamladığınızda, müşteriye fatura yapmayı kabul ediyor. İş için aşağıdaki proje kategorilerini ayarlarsınız, böylece bunları faturalandırma sürecinde kullanabilirsiniz:

- Danışmanlık
- Tasarla
- Yükleme

Her kategori için tamamlanan proje çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplayacak faturalama kurallarını da ayarlarsınız.

Bütçe yöneticisi proje kategorileri için bir bütçe oluşturur. Tamamlanan çalışmanın tutarı otomatik olarak, bütçelenen tutarlarla karşılaştırılan fiili çalışma yüzdesi olarak hesaplanır.

## <a name="prerequisites"></a>Önkoşullar

Faturalama kuralları kullanan bir proje oluşturmadan önce, fatura kuralları için numara serilerini ve hak ediş bazında faturalamayı deftere nakletmek için kullanılan bir ücret günlüğü ayarlamanız gerekir.

1. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** öğesine gidin.
2. **Proje yönetimi ve muhasebe parametreleri** sayfasında, **Numara serileri** sekmesinde, ödeme kuralları oluşturulurken kullanmak istediğiniz numara sırasını ayarlayın.
3. **Proje yönetimi ve muhasebe** \> **Günlükler** \> **Ücret**'e gidin.
4. **Ücret günlüğü** sayfasında, **Yeni**'yi seçin ve günlük adını girin.

## <a name="create-a-contract-for-progress-billings"></a>Hak ediş bazında faturalama için sözleşme oluşturma

Sabit fiyatlı bir proje için proje sözleşmesi oluşturmak için bu yordamı kullanın. Projedeki tamamlanan iş belirtilen yüzdeye ulaştığında proje faturası oluşturursunuz.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri**'ne gidin.
2. **Proje sözleşmeleri** sayfasında, **Yeni**'yi seçin.
3. **Yeni proje sözleşmesi** iletişim kutusunda, aşağıdaki alanları ayarlayın:

    - **Dosya Adı**
    - **Finansman türü**
    - **Finansman kaynağı**
    - **Satış para birimi** – Varsayılan olarak bu para birimi proje sözleşmesiyle ilişkilendirilen müşteri faturaları için kullanılır. Ancak, belirli bir müşteri faturasındaki satış para birimini değiştirebilirsiniz.

4. **Tamam**'ı seçin. Bilgiler **Proje sözleşmeleri** sayfasının başlığına kopyalanır.
5. **Proje sözleşmeleri** sayfasında, proje için gerekli olan diğer bilgileri doldurun.

## <a name="create-a-project-for-progress-billings"></a>Hak ediş bazında faturalama için proje oluşturma

Proje sözleşmesiyle ilişkili proje ve alt projeler oluşturmak için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin.
2. **Tüm projeler** sayfasında, **Yeni**'yi seçin.
3. **Yeni proje** iletişim kutusunda **Proje türü** alanında, **Zaman ve malzeme**'yi seçin.
4. Proje grubu seçin. Proje grubu, gruba atanan projelerle ilgili deftere nakil bilgilerini tanımlar.
5. **Proje oluştur**'u seçin.
6. Proje oluşturulduktan sonra, proje aşamasını **Sürüyor** olarak ayarlayın.

## <a name="create-a-budget-for-a-project"></a>Proje için bütçe oluşturma

Bütçe kategorileri, her kategori için tamamlanan çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplamak için kullanılır. Tahmini maliyetler için bütçe kategorileri oluşturmak üzere bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin.
2. **Tüm projeler** sayfasında, istediğiniz projeyi seçin ve açın.
3. **Projeler** sayfasında, Eylem bölmesinde, **Plan** sekmesinde, **Bütçe** grubunda **Proje bütçesi**'ni seçin.
4. **Proje bütçesi** sayfasında, projedeki her kategori için tahmini bir maliyet girin.

## <a name="create-billing-rules-for-progress-billings"></a>Hak ediş bazında faturalama için fatura kuralları oluşturma

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri**'ne gidin.
2. **Proje sözleşmeleri** sayfasında, bir proje sözleşmesi seçin ve açın.
3. Proje sözleşmesi sayfasında, **Faturalama kuralları** hızlı sekmesinde, **Ekle**'yi seçin.
4. **Faturalama kuralı** sayfasında, **Satır türü** alanında, **İlerleme**'yi seçin.
5. **Faturalama kuralı satırı ayrıntıları** hızlı sekmesinde, **Sözleşme değeri** alanına sözleşmenin toplam değerini girin.
6. **Kategori** alanında, ücret hareketini deftere nakletmek için kategoriyi seçin.
7. **Proje** alanında, bu fatura kuralını kullanan projeyi seçin.
8. İsteğe bağlı: Faturalama kuralını ek projelere atayın. **Proje** hızlı sekmesinde, **Kullanılabilir projeler** bölümünde bir proje seçin ve sonra projeyi **Seçili projeler** bölümüne eklemek için sağ ok düğmesini seçin.
9. İsteğe bağlı: Müşterinin bir faturadaki ödemeler üzerinden tuttuğu yüzde tutarını hesaplayın. **Ödeme bekletme koşulları** hızlı sekmesinde, finansman kaynağını seçin ve **Bekletme yüzdesi** alanına bekletme yüzdesini girin.
10. Proje sözleşmesi için ek faturalama kuralları oluşturmak üzere bu adımları yineleyin.
