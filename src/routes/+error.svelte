<script>
  
    import { page } from '$app/stores'
  
      export let title = `${$page.status} - ${$page.error?.message}`;
  </script>
  
  <div class="">
  <figure
      class=" max-w-4xl mx-auto grid grid-cols-1 py-12 px-4 sm:p-6 md:py-18 md:px-8 bg-slate-100 rounded-xl p-8 md:p-0 dark:bg-slate-800"
  >
      <img
          class="w-28 h-28 md:rounded-none rounded-full mx-auto"
          src="/images/CrowdtainerLogo.svg"
          alt=""
          width="384"
          height="512"
      />
      <div class="pt-6 md:p-8 text-center md:text-left space-y-4">
          <blockquote>
              <p class="dark:text-white text-black text-center text-lg font-medium">
                  {title}
              </p>
          </blockquote>
          <figure>
              <figcaption class="font-medium">
                  <div class="text-center text-sky-500 dark:text-sky-400">No crowdtainers here.</div>
              </figcaption>
          </figure>
      </div>
  </figure>
  
</div>