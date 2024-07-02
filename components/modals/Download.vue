<template>
  <div
    class="modal fade"
    id="downloadModal"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fw-bold fs-5" id="exampleModalLabel">
            Download item ini?
          </h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body my-3">
          <div class="border rounded-4 p-3">
            <div class="d-flex align-items-center gap-3">
              <div class="h-bg-primary-50 d-flex justify-content-center text-center p-2 rounded-2 h-w-12">
                <i class="bi bi-file-earmark-arrow-down"></i>
              </div>
              <p class="h-text-body-16">
                Buku Indikator Hasil Pembangunan Daerah Kabupaten Banyuwangi
                Tahun 2022.pdf
              </p>
            </div>
          </div>
        </div>
        <div class="modal-footer justify-content-center text-center border-top-0 gap-1">
          <button
            type="button"
            class="h-btn-outline--primary"
            data-bs-dismiss="modal"
          >
            Batalkan
          </button>
          <button type="button" class="h-btn--primary">Download</button>
        </div>
      </div>
    </div>
  </div>
</template>
