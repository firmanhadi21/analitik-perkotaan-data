# Analitik Geospasial Perkotaan — paket data

Snapshot data yang dipakai di kursus **Analitik Geospasial Perkotaan** (sigro.id, Firman Hadi) untuk Kota Semarang
dan Kota Makassar. Unduh `analitik-perkotaan-data.zip` dari halaman
[Releases](../../releases/latest), lalu ekstrak ke folder yang sama dengan paket latihan kursus: isinya masuk ke
`urban_analytics/data/raw/`.

Data dibekukan agar angka Anda sama dengan angka di video. OpenStreetMap berubah setiap hari; skrip
`scripts/fetch_osm.py --unduh-ulang` di paket latihan mengambil data terbaru (angkanya akan berbeda).

## Isi

| Berkas (per kota) | Isi |
|---|---|
| `snapshot.json` | Waktu unduh dan jumlah fitur |
| `osm_<kota>.gpkg` | Batas kota, kecamatan, kelurahan, bangunan, POI (OpenStreetMap) |
| `jalan_drive.graphml`, `jalan_walk.graphml` | Jaringan jalan kendaraan dan pejalan kaki (OSMnx) |
| `ghlc/ghlc30_2020…2024.tif`, `ghlc/ghlc10_2020.tif` | Jendela Global Harmonized Land Cover, UTM |

| Kota | Diunduh (UTC) | Kelurahan | Bangunan |
|---|---|---|---|
| Semarang | 2026-09-29 12:21 | 177 | 521.622 |
| Makassar | 2026-09-29 14:42 | 153 | 252.408 |

## Sumber dan lisensi

- **OpenStreetMap** — © kontributor OpenStreetMap, [ODbL 1.0](https://opendatacommons.org/licenses/odbl/).
  Berkas `osm_*.gpkg` dan `jalan_*.graphml` adalah basis data turunan dan tetap berlisensi ODbL.
- **Global Harmonized Land Cover (GHLC)** — OpenGeoHub / LandMetric; Moreno et al. (2026),
  https://doi.org/10.5194/egusphere-2026-5540; data asli: https://source.coop/opengeohub/ogh-ghlc10
  (lihat lisensi di halaman sumber).
