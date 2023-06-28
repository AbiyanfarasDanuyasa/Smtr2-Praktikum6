# Smtr2-Praktikum6

Departemen apa saja yang terlibat dalam tiap-tiap project

```
select p.nama as perusahaan, d.nama as departemen, pr.nama as project from perusahaan p join departemen d on p.id_p = d.id_p join karyawan k on d.id_dept = k.id_dept join project_detail pd on k.nik = pd.nik join project pr on pd.id_proj = pr.id_proj order by pr.nama;
```
![gambar1](https://github.com/AbiyanfarasDanuyasa/Smtr2-Praktikum6/assets/115562487/62155f77-d5e8-44e2-95d5-8cc0c1b945cd)

Jumlah karyawan tiap departemen yang bekerja pada tiap-tiap project

```
select p.nama as perusahaan, d.nama as departemen, pr.nama as project, count(distinct k.nik) as jumlah_karyawan from perusahaan p join departemen d on p.id_p = d.id_p join karyawan k on d.id_dept = k.id_dept join project_detail pd on k.nik = pd.nik join project pr on pd.id_proj = pr.id_proj group by p.nama, d.nama, pr.nama order by pr.nama;

```

![gambar2](https://github.com/AbiyanfarasDanuyasa/Smtr2-Praktikum6/assets/115562487/c5592d58-ead5-40f6-8b43-3a6fa40d8e8b)
