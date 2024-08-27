<script>
  export default {
    data () {
      return {
        dialog: false,
        jobs: ['Marketing Planner', 'UI/UX Content Planner', 'HR/Legal Manager', 'UI/UX Content Writer', 'UI/UX Designer', 'Java Spring Boot'],
        titleJob: '',
				isSelecting: false,
				selectedFile: null
      }
    },

    methods: {
      jobDetail(title) {
        this.dialog = true;
        this.titleJob = title;
        console.log(this.titleJob);
        
      },
			handleFileImport() {
				this.isSelecting = true;

				// After obtaining the focus when closing the FilePicker, return the button state to normal
				window.addEventListener('focus', () => {
						this.isSelecting = false
				}, { once: true });
				
				// Trigger click on the FileInput
				this.$refs.uploader.click();
			},
			onFileChanged(e) {
				this.selectedFile = e.target.files[0];

				// Do whatever you need with the file, liek reading it with FileReader
			},
    }
  }
</script>

<template>
  <v-container >
    <v-row 
    no-gutters
    >
      <v-col
      cols="12"
      sm="5"
      v-for="job in jobs">
        <v-card
        color="lime-lighten-3"
        class="text-center ma-1"
        >
          <v-row>
            <v-col
            cols="5"
            sm="5"
            class="text-left ma-1"
            >
              <h5>{{ job }}</h5>
            </v-col>

            <v-col
            cols="5"
            sm="5"
            class="text-right ma-1">
              <v-btn @click="jobDetail(job)" color="yellow">
                See job
              </v-btn>
            </v-col>
          </v-row>
        </v-card>
      </v-col>

      <!-- <v-dialog
      v-model="dialog"
      width="auto">
        <v-card 
        title={{ titleJob }}
        >
          <v-card-text>
            wdom
          </v-card-text>

          

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
              text="Submit"
              @click="isActive.value = false"
            ></v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog> -->

    <v-dialog
      v-model="dialog"
      width="auto"
    >
      <v-card
        width="850"
        color="lime-lighten-3"
      >
				<v-card-title
				class="text-green-darken-2">
					{{ titleJob }}
				</v-card-title>

        <v-card-text>
          <v-row>
            <v-col
            cols="12"
            sm="12">

              <h4><b>Job Description :</b></h4>
              <ul>
                <li>Monitor competition to identify new industry trends and opportunities for innovation</li>
                <li>Develop marketing strategies based on customer preferences, business objectives, and available resources</li>
                <li>Conduct market research to identify potential customers and assess their needs, interests, and preferences</li>
                <li>Work with design teams to develop marketing materials such as brochures, ads, and presentations</li>
                <li>Create an advertising budget that reflects the company’s priorities while remaining within the parameters set by upper management</li>
                <li>Provide feedback to superiors regarding the effectiveness of new campaigns and recommend adjustments</li>
              </ul>

              <br>

              <h4><b>Skills :</b></h4>
              <ul>
                <li>Minimum bachelor degree in Marketing Management;</li>
                <li>Minimum 3-5 years experience as Marketing Manager/Director in any marketplace industry;</li>
                <li>Good time management and project management skill;</li>
                <li>Creative communication skill in both verbal and design</li>
                <li>Create an advertising budget that reflects the company’s priorities while remaining within the parameters set by upper management</li>
                <li>Multi-language abilities in verbal and non-verbal</li>
              </ul>
            </v-col>
          </v-row>
          <v-divider
          class="my-2"></v-divider>
          <v-row>
            <v-col
            cols="12"
            sm="12">
              <h4><b>Send Your Job Application</b></h4>
            </v-col>

            <v-col
            cols="6"
            sm="6">
              <v-text-field
                label="Your Name"
                hide-details
                required
              ></v-text-field>
            </v-col>

            <v-col
            cols="6"
            sm="6">
              <v-text-field
                label="Mobile Number"
                hide-details
                required
              ></v-text-field>
            </v-col>

            <v-col
            cols="6"
            sm="6">
              <v-text-field
                label="Email Address"
                hide-details
                required
              ></v-text-field>
            </v-col>

            <v-col
            cols="6"
            sm="6">
              <v-text-field
                label="Write your message here..."
                required
              ></v-text-field>
            </v-col>

            <v-col
            cols="12"
            sm="12">
							<v-btn 
							prepend-icon="mdi-upload" 
							stacked color="orange" 
							class="text-white"
							:loading="isSelecting" 
							@click="handleFileImport"
							>
							</v-btn>

							<input 
							ref="uploader" 
							class="d-none" 
							type="file" 
							@change="onFileChanged"
							>
						</v-col>
          </v-row>

					<v-btn
            text="Send Message"
            @click="dialog = false"
						color="grey"
						class="text-white mt-2"
          ></v-btn>

        </v-card-text>

        
      </v-card>
    </v-dialog>
    </v-row>
  </v-container>
  
</template>