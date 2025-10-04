🧩 ETL Satış Segmentasyonu (SSIS + SQL Server Agent)
📌 Proje Özeti

Bu proje, SQL Server Integration Services (SSIS) kullanılarak geliştirilmiş bir ETL (Extract–Transform–Load) sürecidir.
Amaç, satış verilerini tutar miktarına göre üç segmente ayırmak ve bu verileri SQL Server’daki ilgili tablolara aktarmaktır:

Yüksek Satışlar (SalesHigh)

Orta Satışlar (SalesMedium)

Düşük Satışlar (SalesLow)

⚙️ Süreç Akışı

Kaynak: Flat File (CSV)

Dönüşüm Adımları:

Data Conversion → veri tipleri uygun formata dönüştürülür

Conditional Split → satış tutarına göre üç farklı akış oluşturulur

Hedef Tablolar:

dbo.SalesHigh

dbo.SalesMedium

dbo.SalesLow

🕒 Zamanlayıcı (SQL Server Agent)

ETL paketi, SQL Server Agent üzerinden zamanlanmış bir job ile otomatik olarak çalıştırılmaktadır.

Job Adı: ETL_Sales_Schedule

Çalışma Sıklığı: Haftada bir defa (otomatik olarak belirli gün/saatte çalışır)

Durum: ✅ Başarılı (job test edilip çalışması doğrulanmıştır)

Bu sayede, veri yükleme süreci manuel müdahale olmadan düzenli olarak yürütülür.
