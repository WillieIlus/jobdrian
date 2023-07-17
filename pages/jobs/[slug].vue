<template>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
    <CardBase class="col-span-3 md:col-span-2 bg-white p-7 flex flex-col justify-center">
      <div class="space-y-8">
        <CardDescription>
          <template #title>
            Job Description
          </template>
          <template #content>

            <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti placeat esse, dicta architecto laboriosam
            aliquam a ipsa. Laboriosam temporibus officiis suscipit in id magni, commodi nam, at atque corporis
            architecto!
            </p>
          </template>
        </CardDescription>
        <CardDescription>
          <template #title>
            Job Qualification
          </template>
          <template #content>
            <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti placeat esse, dicta architecto laboriosam
            aliquam a ipsa. Laboriosam temporibus officiis suscipit in id magni, commodi nam, at atque corporis
            architecto!
            </p>
            <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti placeat esse, dicta architecto laboriosam
            aliquam a ipsa. Laboriosam temporibus officiis suscipit in id magni, commodi nam, at atque corporis
            architecto!
            </p>
            <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti placeat esse, dicta architecto laboriosam
            aliquam a ipsa. Laboriosam temporibus officiis suscipit in id magni, commodi nam, at atque corporis
            architecto!
            </p>
          </template>
        </CardDescription>
        <CardDescription>
          <template #title>Required Skills</template>
          <template #content>
            <div class="flex space-x-4">
              <ButtonGreen />
              <ButtonBlue />
              <ButtonRed />
              <ButtonOrange />
            </div>
          </template>
        </CardDescription>
      </div>
    </CardBase>
    <CardBase class="col-span-3 md:col-span-1 p-4 flex flex-col justify-center">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div class="flex items-center">
          <div class="w-9 h-9 text-indigo-900">
            <CalendarIcon />
          </div>
          <div class="ml-4">
            <div class="text-sm text-indigo-900">Date Posted</div>
            <div class="text-sm text-indigo-300">2021-09-01</div>
          </div>
        </div>
        <div class="flex items-center">
          <div class="w-9 h-9 text-indigo-900">
            <ClockIcon />
          </div>
          <div class="ml-4">
            <div class="text-sm text-indigo-900">Expiration Date</div>
            <div class="text-sm text-indigo-300">2021-09-01</div>
          </div>
        </div>
        <div class="flex items-center">
          <div class="w-9 h-9 text-indigo-900">
            <MapIcon />
          </div>
          <div class="ml-4">
            <div class="text-sm text-indigo-900">Location</div>
            <div class="text-sm text-indigo-300">Manila, Philippines</div>
          </div>
        </div>
        <div class="flex items-center">
          <div class="w-9 h-9 text-indigo-900">
            <BriefcaseIcon />
          </div>
          <div>
            <div class="text-sm text-indigo-900">Work Hours</div>
            <div class="text-sm text-indigo-300">8 hours</div>
          </div>
        </div>
        <div class="flex items-center">
          <div class="w-9 h-9 text-indigo-900">
            <CurrencyDollarIcon />
          </div>
          <div>
            <div class="text-sm text-indigo-900">Salary</div>
            <div class="text-sm text-indigo-300">Php 20,000</div>
          </div>
        </div>
      </div>

      <ButtonGreen class="mt-4">
        Apply for Job
      </ButtonGreen>
    </CardBase>
  </div>
</template>

<script setup>
import { CalendarIcon, BriefcaseIcon, MapIcon, ClockIcon, CurrencyDollarIcon } from '@heroicons/vue/24/outline'
</script>
