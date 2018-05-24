---
title: "Yük kullanımını zamanla"
description: "Bu konu bir ambar için yükün nasıl ayarlanacağını ve zamanlanacağını açıklar."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9bb8f84bd038c6bc59ef23d6471a9481c904bdb6
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a>Yük kullanımını zamanla

[!include[banner](../includes/banner.md)]

Seçilen yerleşim türleri için yük kullanımını zamanlayabilir ve geçerli ve gelecekteki yük kullanımını da planlayabilirsiniz. Bir veya daha fazla tesis, yük birimleri (bölge veya ambar) veya bir bölge ve ambar birleşimi için yükü planlayabilirsiniz.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Bir ambar veya tesis için yükü zamanlama ve görüntüleme

Tesisler, ambarlar veya bölgeler için yükü zamanlamak için bir alan kullanım kurulumu oluşturun ve bunu bir master plan ile ilişkilendirin.

Alan kullanımı kurulumunda, alan kullanımının nasıl planlanacağını belirtmek için **Toplu yerleşim** ve **Malzeme çekme yerleşimi** gibi yerleşim türleri kullanın. **Bölge** gibi bir depolama yük modu belirtin.

Gelecekteki alan kullanımı planlaması ilişkilendirilen master planda hesaplanan bilgileri temel alır. Master plan üretim ve işlemler için gelen ve giden siparişlere yönelik kaynak planlamasını tahmin eder. Kullanılabilir alan planlaması seçili master plan ile alan kullanımı kurulumu arasındaki ilişkiyi temel alır.

Yer kullanımı kurulumunda seçtiğiniz depolama yükü modunu kullanarak yükün her ambar veya bölge için mi planlanacağını veya planlamaların ambarlar ve bölgeler hakkında daha fazla bilgi içermesi gerekip gerekmediğini belirtebilirsiniz. Ayrıca engellenen yerleşimlerin yük kullanımı hesaplaması dışında tutulup tutulmayacağını da belirtebilirsiniz.

Alan kullanımını **Ambar yük kullanımı** raporu oluşturarak planlayabilirsiniz. Bu raporu oluşturduğunuzda, yük kullanımının her tesis için mi, tesisler arasında mı yoksa bölge veya ambar gibi seçilen yük birimi için mi planlanması gerektiğini belirtebilirsiniz.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Ambar için alan kullanım kurulumu oluşturma

1. **Stok yönetimi** \> **Kurulum** \> **Ambar izleme** \> **Alan kullanımı**'nı seçin.
2. Alan kullanımı kurulumu oluşturmak için **Yeni**'yi seçin. Bir kurulum için bir kod veya bir ad belirtin.
3. **Depolama yükü modu** alanında, alan kullanımına genel bakışın bilgileri ambara, bölgeye veya ambar ve bölgeye göre mi göstermesi gerektiğini seçin.
4. Engellenen stok yerleşimlerini kullanılabilir alan hesaplaması dışında tutmak için **Engellenen yerleşimleri hariç tut** seçeneğini **Evet** olarak ayarlayın. **Stok yerleşimleri** sayfasındaki **Diğer** hızlı sekmesinde bulunan **Giriş engellendi** veya **Çıkış engellendi** alanında yerleşim için bir engelleme nedeni belirterek girdi ve çıktı için bir stok yerleşimini engelleyebilirsiniz.
5. **Yerleşim türü** hızlı sekmesinde alan kullanımı hesaplamalarına dahil edilecek yerleşim türlerini seçin. Planlama için en az bir yerleşim türü seçmelisiniz.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Bir alan kullanım kurulumunu bir master plan ile ilişkilendirme

1. **Stok Yönetimi** \> **Periyodik görevler** \> **Yük kullanımını zamanla**'yı seçin.
2. **Master plan** alanında bir master plan seçin.
3. **Gün sayısı** alanında, geçerli ve gelecekteki iş yüklerinin planlanmasına dahil edilecek gün sayısını belirtin.
4. **Alan kullanımı** alanında, geçerli ve gelecekteki iş yüklerinin planlanması için kullanılacak alan kullanımı kurulumunu seçin.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Yük kullanım planlamasını belirtme ve bilgileri görüntüleme

1. **Stok Yönetimi** \> **Sorgular ve raporlar** \> **Fiziksel stok raporları** \> **Ambar yük kullanımı**'nı seçin.
2. **Gösterme ölçütü** alanında, alan kullanımı planlaması düzeyini seçin:

    - **Tesis** – Her tesis için alan kullanımını yansıtır. Bu yansıtma, örneğin, bir tesis için tüm ambarları görüntülemek istediğinizde yararlıdır; böylece, ambarlar arasında alan kullanımını dengeleyebilirsiniz.
    - **Yük birimi** – Bölgeler veya alanlar için alan kullanımını yansıtır. Kullanılabilir alan, alan kullanımı kurulumunu oluştururken **Alan kullanımı** sayfasındaki **Depolama yükü modu** alanında seçtiğiniz değere göre yansıtılır.

3. Önceki adımda seçtiğiniz değere bağlı olarak, aşağıdaki adımlardan birini izleyin:

    - **Gösterme ölçütü** alanında **Tesis**'i seçtiyseniz **Tesis** alanı kullanılabilir. Yansıtmaya dahil edilecek bir veya daha fazla tesis seçin.
    - **Gösterme ölçütü** alanında **Yük birimi**'ni seçtiyseniz **Yük birimi** alanı kullanılabilir. Yük birimini seçin.

4. **Yükleme türü** alanında alanın planlanacağı ambar işletme birimini belirtmek **Hacim** veya **Ağırlık** seçeneğini belirtin.
5. **Alan kullanımı kurulumu** alanında, yansıtmanın temel alacağı alan kullanımı kurulumunu seçin.

