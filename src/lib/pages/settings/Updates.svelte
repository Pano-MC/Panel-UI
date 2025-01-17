<!-- Updates Sub Page -->

<div class="container">
  <!-- Action Menu -->
  <PageActions>
    <div slot="left">
      <span
        class="small"
        use:tooltip="{['Last Check', { placement: 'bottom' }]}">
        <i class="fa-regular fa-clock me-2"></i>
        DATE
      </span>
    </div>
    <button type="button" class="btn btn-secondary">
      <i class="fas fa-rotate me-2"></i>
      Check Updates
    </button>
    <div slot="right">
      <button type="button" class="btn btn-link">Update All</button>

      <button class="btn btn-secondary">
        <i class="fa-regular fa-arrows-rotate me-2"></i> Check Updates
      </button>
    </div>
  </PageActions>

  <div
    class="alert alert-warning mb-3 animate__animated animate__bounceInDown animate__slower"
    role="alert">
    <h5 class="alert-heading">Yenide başlatma bekleniyor</h5>

    <p>
      Platform güncellemesinin uygulanabilmesi için yeniden başlatma gerekiyor.
      Yönetim Paneli ve Website bakım moduna alınacak, oyun sunucuları
      etkilenmeyecek.
    </p>
    <p>
      Tahmini süre: <b>TIME</b>
    </p>
    <button class="btn btn-outline-primary" type="button">
      <i class="fa-solid fa-power-off me-2"></i>
      Yeniden Başlat</button>
  </div>

  <div class="card">
    <div class="card-body">
      <CardHeader>
        <h5 class="card-title" slot="left">Available Updates (COUNT)</h5>
        <!-- Filters -->
        <CardFilters slot="right">
          <CardFiltersItem href="/">Tümü</CardFiltersItem>
          <CardFiltersItem href="/">Platform</CardFiltersItem>
          <CardFiltersItem href="/">Eklenti</CardFiltersItem>
        </CardFilters>
      </CardHeader>

      <!-- Pending Update Card -->
      <div class="card border">
        <div class="card-body">
          <div class="row d-flex flex-nowrap">
            <div class="col-auto d-md-flex d-none">
              <a href="/">
                <img
                  height="128"
                  width="128"
                  src="..."
                  class="img-thumbnail animate__animated animate__zoomIn d-block"
                  alt="Alt" />
              </a>
            </div>
            <div class="col">
              <div class="row">
                <div class="col">
                  <a href="/">
                    <h5 class="card-title">ID</h5>
                  </a>
                </div>
                <div class="col-auto">
                  <button class="btn btn-sm btn-primary" type="button"
                    >Update</button>
                </div>
                <div class="col-auto ps-0">
                  <a
                    href="#"
                    tabindex="0"
                    class="link-danger"
                    data-bs-toggle="popover"
                    data-bs-trigger="focus"
                    data-bs-custom-class="font-monospace"
                    data-bs-title="Error Log"
                    data-bs-content="ERR LOG">
                    <i class="fa-solid fa-circle-exclamation fa-1x"></i>
                  </a>
                </div>
              </div>
              <small class="text-muted">
                <span class="font-monospace">TYPE</span>
                <div class="vr mx-2"></div>
                <span class="font-monospace"
                  >OLDV <i class="fa-solid fa-caret-right"></i> NEWV</span>
                <div class="vr mx-2"></div>
                <span class="font-monospace">SIZE</span>
                <div class="vr mx-2"></div>
                <span class="font-monospace text-black">INSTALLING...</span>
                <span class="font-monospace text-black">DOWNLOADING...</span>
              </small>
              <span class="font-monospace">
                <div
                  class="progress my-3"
                  role="progressbar"
                  aria-label="Example 1px high"
                  aria-valuenow="25"
                  aria-valuemin="0"
                  aria-valuemax="100"
                  style="height: 3px">
                  <div class="progress-bar bg-secondary" style="width: 25%">
                  </div>
                </div>
              </span>

              <details>
                <summary class="pb-3"> View Changelog</summary>
                <p>CHANGELOG</p>
              </details>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<script>
  import { getContext } from "svelte";
  import tooltip from "$lib/tooltip.util";
  import PageActions from "$lib/component/PageActions.svelte";
  import CardHeader from "$lib/component/CardHeader.svelte";
  import CardFiltersItem from "$lib/component/CardFiltersItem.svelte";
  import CardFilters from "$lib/component/CardFilters.svelte";

  const pageTitle = getContext("pageTitle");

  pageTitle.set("Güncellemeler");
</script>
