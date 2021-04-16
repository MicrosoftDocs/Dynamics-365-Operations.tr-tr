---
title: Satıcı tasarımları arasında geçiş yapma
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında satıcı verisi tümleştirmesi arasında geçiş yapmayı açıklar.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750606"
---
# <a name="switch-between-vendor-designs"></a>Satıcı tasarımları arasında geçiş yapma

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Satıcı veri akışı 

**Kuruluş** türünün satıcılarını depolamak için **Hesap** tablosunu ve **Kişi** türündeki satıcıları depolamak için **İlgili Kişi** tablosunu kullanmayı seçerseniz, aşağıdaki iş akışlarını yapılandırın. Aksi takdirde, bu yapılandırmaya gerek yoktur.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Organizasyon türündeki satıcılar için genişletilmiş satıcı tasarımını kullan

**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir. Her şablon için bir iş akışı oluşturacaksınız.

+ Hesaplar Tablosunda Satıcılar oluşturma
+ Satıcılar Tablosunda Satıcılar oluşturma
+ Hesaplar Tablosunda Satıcıları Güncelleştirme
+ Satıcılar Tablosunda Satıcıları Güncelleştirme

İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.

1. **Satıcı** tablosu için bir iş akışı işlemi oluşturun ve **Hesaplar Tablosunda Satıcılar Oluşturma** iş akışı işlemi şablonunu seçin. Daha sonra **Tamam**'ı seçin. Bu iş akışı **Hesap** tablosu için satıcı oluşturma senaryosunu işler.

    ![Hesaplar Tablosunda Satıcılar Oluşturma iş akışı işlemi](media/create_process.png)

2. **Satıcı** tablosu için bir iş akışı işlemi oluşturun ve **Hesaplar Tablosunda Satıcıları Güncelleştirme** iş akışı işlemi şablonunu seçin. Daha sonra **Tamam**'ı seçin. Bu iş akışı **Hesap** tablosu için satıcı güncelleştirme senaryosunu işler.
3. **Hesap** tablosu için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Satıcılar Oluşturma** iş akışı işlemi şablonunu seçin.
4. **Hesap** tablosu için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Satıcıları Güncelleştirme** iş akışı işlemi şablonunu seçin.
5. İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz. Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.

    ![Arka plan iş akışına dönüştürme düğmesi](media/background_workflow.png)

6. **Kuruluş** türünde satıcılarla ilgili bilgileri depolamak üzere **Hesap** tablosunu kullanmaya başlamak için **Hesap** ve **Satıcı** tablolarına yönelik olarak oluşturduğunuz iş akışlarını etkinleştirin.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Kişi türündeki satıcılar için genişletilmiş satıcı tasarımını kullan

**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir. Her şablon için bir iş akışı oluşturacaksınız.

+ Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma
+ İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma
+ İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme
+ Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme

İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.

1. **Satıcı** tablosu için yeni bir iş akışı işlemi oluşturun ve **İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma** iş akışı işlemi şablonunu seçin. Daha sonra **Tamam**'ı seçin. Bu iş akışı **İlgili kişi** tablosu için satıcı oluşturma senaryosunu işler.
2. **Satıcı** tablosu için yeni bir iş akışı işlemi oluşturun ve **İlgili Kişiler Tablosunda Kişi türünde Satıcıları güncelleştirme** iş akışı işlemi şablonunu seçin. Daha sonra **Tamam**'ı seçin. Bu iş akışı **İlgili kişi** tablosu için satıcı güncelleştirme senaryosunu işler.
3. **İlgili Kişi** tablosu için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma** şablonunu seçin.
4. **İlgili Kişi** tablosu için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Kişi türünde Satıcıları güncelleştirme** şablonunu seçin.
5. İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz. Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.
6. **Kişi** türünde satıcılarla ilgili bilgileri depolamak üzere **İlgili Kişi** tablosunu kullanmaya başlamak için **İlgili Kişi** ve **Satıcı** tablolarına yönelik olarak oluşturduğunuz iş akışlarını etkinleştirin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]