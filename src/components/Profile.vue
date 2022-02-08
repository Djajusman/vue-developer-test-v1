<template>
  <div class="page-holder bg-gray-100">
    <div class="container-fluid px-lg-4 px-xl-5 contentDiv">
      <!-- Page Header-->
      <div class="page-header mb-4">
        <h1 class="page-heading">Profile</h1>
      </div>
      <section>
        <div class="row">
          <div class="col-lg-4">
            <div class="card card-profile mb-4">
              <div class="card-header" style="background-image: url()"></div>
              <div class="card-body text-center">
                <img
                  class="card-profile-img"
                  src="../assets/foto-profile.jpg"
                  alt="Riyadh Tsaniyadi Djajusman"
                />
                <h3 class="mb-3">Riyadh Tsaniyadi Djajusman</h3>
                <p class="mb-4">Frontend Developer</p>
              </div>
            </div>
          </div>
          <div class="col-lg-8">
            <form class="card mb-4">
              <div class="card-header">
                <h4 class="card-heading">Candidate Profile</h4>
              </div>
              <div class="card-body">
                <div class="form-group row">
                  <label class="col-sm-3 col-form-label">
                    Place & Date of Birth
                  </label>
                  <div class="col-sm-9">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Tanjung Enim, 05 Oktober 1999"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-3 col-form-label">Nationality</label>
                  <div class="col-sm-9">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Indonesia"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-3 col-form-label">Sex</label>
                  <div class="col-sm-9">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Male"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-3 col-form-label">Marital Status</label>
                  <div class="col-sm-9">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Single"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-3 col-form-label">Health</label>
                  <div class="col-sm-9">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Good"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <div class="col-sm-12">
                    <textarea
                      class="form-control-plaintext mb-2"
                      rows="4"
                      placeholder="Here can be your description"
                    >
I am a AD Mechatronics graduate with a strong interest in Information Technology. Styled with hands on various activities such as bussines. I am skilled at organizing people, solving a problem and doing multiple tasks.</textarea
                    >
                  </div>
                </div>
              </div>
            </form>
          </div>
        </div>
      </section>
      <section>
        <div class="row">
          <div class="col-lg-4"></div>
          <div class="col-lg-8">
            <form class="card mb-4">
              <div class="card-header">
                <h4 class="card-heading">Personal Contact</h4>
              </div>
              <div class="card-body">
                <div class="form-group row">
                  <label class="col-sm-2 col-form-label">Call Number</label>
                  <div class="col-sm-10">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": +62 822 1958 7748"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-2 col-form-label">Email</label>
                  <div class="col-sm-10">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": tsaniyadiriyadh@gmail"
                    />
                  </div>
                </div>
                <div class="form-group row">
                  <label class="col-sm-2 col-form-label">Address</label>
                  <div class="col-sm-10">
                    <input
                      type="text"
                      readonly
                      class="form-control-plaintext mb-2"
                      id="staticEmail"
                      value=": Bandung, West Java"
                    />
                  </div>
                </div>
              </div>
            </form>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
<style>
.card-header:first-child {
  border-radius: calc(1rem - 1px) calc(1rem - 1px) 0 0;
}

.card-header {
  position: relative;
  padding: 2rem 2rem;
  border-bottom: none;
  background-color: white;
  box-shadow: 0 0.125rem 0.25rem rgb(0 0 0 / 8%);
  z-index: 2;
}

.card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #fff;
  background-clip: border-box;
  border: none;
  box-shadow: 0 0.5rem 1rem rgb(0 0 0 / 15%);
  border-radius: 1rem;
}

.bg-gray-100 {
  background-color: #f8f9fa !important;
}

body {
  font-family: 'Poppins' !important;
}

.text-primary {
  color: #4650dd !important;
}

h1,
.h1,
h2,
.h2,
h3,
.h3,
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  line-height: 1.2;
}
.text-muted {
  color: #6c757d !important;
}

.lead {
  font-size: 1.125rem;
  font-weight: 300;
}

.text-sm {
  font-size: 0.7875rem !important;
}

h3,
.h3 {
  font-size: 1.575rem;
}

.page-holder {
  display: flex;
  overflow-x: hidden;
  width: 100%;
  min-height: calc(100vh - 72px);

  flex-wrap: wrap;
}

.card-profile-img {
  position: relative;
  max-width: 8rem;
  margin-top: -6rem;
  margin-bottom: 1rem;
  border: 3px solid #fff;
  border-radius: 100%;
  box-shadow: 0 0.5rem 1rem rgb(0 0 0 / 15%);
  z-index: 2;
}

img,
svg {
  vertical-align: middle;
}

.avatar.avatar-lg {
  width: 5rem;
  height: 5rem;
  line-height: 5rem;
}

.avatar {
  display: inline-block;
  position: relative;
  width: 3rem;
  height: 3rem;
  text-align: center;
  border: #dee2e6;
  border-radius: 50%;
  background: #fff;
  box-shadow: 0 0.5rem 1rem rgb(0 0 0 / 15%);
  line-height: 3rem;
}

.form-control {
  color: #343a40;
}

.page-heading {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  font-weight: 300;
}

.contentDiv {
  padding-top: 4rem;
}

.card-profile .card-header {
  height: 9rem;
  background-position: center center;
  background-size: cover;
}
</style>
<script>
//importing bootstrap 5 Modules
import 'bootstrap/dist/css/bootstrap.min.css'
export default {}
</script>
