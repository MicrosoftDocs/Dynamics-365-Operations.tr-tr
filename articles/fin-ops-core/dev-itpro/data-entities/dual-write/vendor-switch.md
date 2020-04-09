---
title: Satıcı tasarımları arasında geçiş yapma
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında satıcı verisi tümleştirmesi arasında geçiş yapmayı açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173051"
---
# <a name="switch-between-vendor-designs"></a>Satıcı tasarımları arasında geçiş yapma

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Satıcı veri akışı 

**Organizasyon** türünün satıcılarını depolamak için **firma** varlığını ve **kişi** türündeki satıcıları depolamak için ilgili **kişi** varlığını kullanmayı seçerseniz, aşağıdaki iş akışlarını konfigüre edin. Aksi takdirde, bu yapılandırmaya gerek yoktur.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Organizasyon türündeki satıcılar için genişletilmiş satıcı tasarımını kullan

**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir. Her şablon için bir iş akışı oluşturacaksınız.

+ Hesap Varlığında Satıcılar oluşturma
+ Satıcılar varlığında satıcılar oluşturma
+ Hesap Varlığında Satıcılar güncelleme
+ Satıcılar varlığında satıcılar güncelleme

İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.

1. **Hesap Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın. Daha sonra **Tamam**'ı seçin. Bu iş akışı **Hesap** varlığı için satıcı oluşturma senaryosunu işler.

    ![Hesap Varlığında Satıcılar iş akışı süreci oluşturma](media/create_process.png)

2. **Hesap Varlığında Satıcılar Güncelleme** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın. Daha sonra **Tamam**'ı seçin. Bu iş akışı **Hesap** varlığı için satıcı güncelleştirme senaryosunu işler.
3. **Satıcılar Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Firma** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.
4. **Satıcılar Varlığında Satıcılar Güncelleme** iş akışı işlemi şablonunu kullanarak **Firma** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.
5. İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz. Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.

    ![Arka plan iş akışına dönüştürme düğmesi](media/background_workflow.png)

6. **Kuruluş** türünün satıcı bilgilerini depolamak için **Firma** varlığını kullanmaya başlamak için **Firma** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Kişi türündeki satıcılar için genişletilmiş satıcı tasarımını kullan

**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir. Her şablon için bir iş akışı oluşturacaksınız.

+ Satıcı varlığındaki kişi türünden satıcılar oluştur
+ İlgili kişiler varlığındaki kişi türünden satıcılar oluştur
+ İlgili kişiler varlığındaki kişi türünden satıcılar güncelle
+ Satıcı varlığındaki kişi türünden satıcılar güncelle

İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.

1. **İlgili kişiler varlığındaki kişi türünden satıcılar oluştur** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun. Daha sonra **Tamam**'ı seçin. Bu iş akışı **İlgili kişi** varlığı için satıcı oluşturma senaryosunu işler.
2. **İlgili kişiler varlığındaki kişi türünden satıcılar güncelle** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun. Daha sonra **Tamam**'ı seçin. Bu iş akışı **İlgili kişi** varlığı için satıcı güncelleştirme senaryosunu işler.
3. **Satıcı varlığındaki kişi türünden satıcılar oluştur** iş akışı işlemi şablonunu kullanarak **İlgili kişi** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.
4. **Satıcı varlığındaki kişi türünden satıcılar güncelle** iş akışı işlemi şablonunu kullanarak **İlgili kişi** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.
5. İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz. Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.
6. **Kişi** türünün satıcı bilgilerini depolamak için **İlgili kişi** varlığını kullanmaya başlamak için **İlgili kişi** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin.
