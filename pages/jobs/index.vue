<template>
  <div class="flex flex-col">
    <div class="flex mb-4 mt-16">
      <FormSearch />
    </div>
    <div class="flex">
      <div class="w-1/4 px-10">
        Filter List
      </div>
      <div class="w-3/4 px-10">
        Showing 01-12 of 96 jobs
      </div>
    </div>
    <div class="flex gap-2">
      <div class="w-1/4">
        <FilterCategories :categories="categories" />
        <FilterLocations :locations="locations" />
      </div>
      <div class="w-3/4">
        <JobList :jobs="jobs" />
      </div>
    </div>
  </div>
</template>
<script setup>
const categories = ref([
  {
    id: 1,
    name: 'Art & Design',
    slug: 'art-design',
    job_count: 10
  },
  {
    id: 2,
    name: 'Education',
    slug: 'education',
    job_count: 20
  },
  {
    id: 3,
    name: 'Engineering',
    slug: 'engineering',
    job_count: 30
  },
  {
    id: 4,
    name: 'Healthcare',
    slug: 'healthcare',
    job_count: 40
  },
  {
    id: 5,
    name: 'Information Technology',
    slug: 'information-technology',
    job_count: 50
  },
  {
    id: 6,
    name: 'Marketing',
    slug: 'marketing',
    job_count: 60
  },
  {
    id: 7,
    name: 'Sales',
    slug: 'sales',
    job_count: 70
  },
  {
    id: 8,
    name: 'Science',
    slug: 'science',
    job_count: 80
  },
  {
    id: 9,
    name: 'Transportation',
    slug: 'transportation',
    job_count: 90
  },
  {
    id: 10,
    name: 'Writing',
    slug: 'writing',
    job_count: 100
  }

])

const locations = ref([
  {
    id: 1,
    name: 'New York',
    slug: 'new-york',
    job_count: 10
  },
  {
    id: 2,
    name: 'Los Angeles',
    slug: 'los-angeles',
    job_count: 20
  },
  {
    id: 3,
    name: 'Chicago',
    slug: 'chicago',
    job_count: 30
  },
  {
    id: 4,
    name: 'Houston',
    slug: 'houston',
    job_count: 40
  },
  {
    id: 5,
    name: 'Phoenix',
    slug: 'phoenix',
    job_count: 50
  },
  {
    id: 6,
    name: 'Philadelphia',
    slug: 'philadelphia',
    job_count: 60
  },
  {
    id: 7,
    name: 'San Antonio',
    slug: 'san-antonio',
    job_count: 70
  },
  {
    id: 8,
    name: 'San Diego',
    slug: 'san-diego',
    job_count: 80
  },
  {
    id: 9,
    name: 'Dallas',
    slug: 'dallas',
    job_count: 90
  },
  {
    id: 10,
    name: 'San Jose',
    slug: 'san-jose',
    job_count: 100
  }

])

const jobs = ref([
{
    id: 1,
    title: 'Senior Product Designer',
    slug: 'senior-product-designer',
    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, diam id aliquam ultrices, nisl nisi tincidunt enim, vitae ullamcorper velit nunc eget nunc. Donec euismod, diam id aliquam ultrices, nisl nisi tincidunt enim, vitae ullamcorper velit nunc eget nunc.',
    job_type: 'Full Time', // Add the job_type field
    published_at: '2023-07-16T12:00:00Z', // Replace this with the actual date and time
    vacancy: 1,
    salary: 50000, // Replace this with the actual salary amount
    experience: 5, // Replace this with the actual experience required
    category: 'Art & Design', // Add the category field
    company: 'Company A', // Replace this with the actual company name
    location: 'New York', // Add the location field
    image: 'path/to/image.jpg', // Replace this with the actual image path
    is_published: true,
    last_date: '2023-08-15', // Replace this with the actual last date for applications
    created_at: '2023-07-15T08:00:00Z', // Replace this with the actual creation date and time
    updated_at: '2023-07-16T10:00:00Z', // Replace this with the actual update date and time
    active: true,
    views_count: 100,
    click_count: 20,
    featured: false,
    paid: true,
    paid_amount: 50.00, // Replace this with the actual paid amount
    paid_at: '2023-07-16T08:00:00Z', // Replace this with the actual paid date and time
    paid_until: '2023-08-16T08:00:00Z', // Replace this with the actual paid until date and time
    phone_number: '123-456-7890', // Add the phone_number field
    address: '123 Main St, New York, NY', // Replace this with the actual address
    email: 'example@example.com', // Replace this with the actual email
    author: 'John Doe', // Replace this with the actual author name
    openings: 5, // Add the openings field
  },
  {
    id: 7,
    title: 'Web Developer',
    slug: 'web-developer',
    description: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Fusce ac malesuada justo.',
    job_type: 'Part Time',
    published_at: '2023-07-18T10:00:00Z',
    vacancy: 2,
    salary: 60000,
    experience: 3,
    category: 'Information Technology',
    company: 'Company B',
    location: 'San Francisco',
    image: 'path/to/image.jpg',
    is_published: true,
    last_date: '2023-08-20',
    created_at: '2023-07-17T15:30:00Z',
    updated_at: '2023-07-18T09:45:00Z',
    active: true,
    views_count: 80,
    click_count: 15,
    featured: true,
    paid: false,
    paid_amount: 0,
    paid_at: null,
    paid_until: null,
    phone_number: '987-654-3210',
    address: '456 Oak St, San Francisco, CA',
    email: 'webdev@example.com',
    author: 'Jane Smith',
    openings: 3,
  },

  {
    id: 8,
    title: 'Marketing Specialist',
    slug: 'marketing-specialist',
    description: 'Nunc id sapien ac ipsum venenatis faucibus vel sit amet nunc. Morbi ullamcorper, sapien nec accumsan bibendum, odio purus sagittis odio, euismod consectetur mi neque a est.',
    job_type: 'Full Time',
    published_at: '2023-07-20T14:20:00Z',
    vacancy: 1,
    salary: 75000,
    experience: 5,
    category: 'Marketing',
    company: 'Company C',
    location: 'Los Angeles',
    image: 'path/to/image.jpg',
    is_published: true,
    last_date: '2023-08-30',
    created_at: '2023-07-19T12:15:00Z',
    updated_at: '2023-07-20T10:30:00Z',
    active: true,
    views_count: 120,
    click_count: 25,
    featured: false,
    paid: true,
    paid_amount: 100.00,
    paid_at: '2023-07-20T09:00:00Z',
    paid_until: '2023-08-20T09:00:00Z',
    phone_number: '555-123-4567',
    address: '789 Elm St, Los Angeles, CA',
    email: 'marketing@example.com',
    author: 'Michael Johnson',
    openings: 1,
  },

  {
    id: 9,
    title: 'Graphic Designer',
    slug: 'graphic-designer',
    description: 'Donec euismod, diam id aliquam ultrices, nisl nisi tincidunt enim, vitae ullamcorper velit nunc eget nunc. Sed euismod, diam id aliquam ultrices, nisl nisi tincidunt enim, vitae ullamcorper velit nunc eget nunc.',
    job_type: 'Freelance',
    published_at: '2023-07-22T09:10:00Z',
    vacancy: 3,
    salary: 40000,
    experience: 2,
    category: 'Art & Design',
    company: 'Company D',
    location: 'Chicago',
    image: 'path/to/image.jpg',
    is_published: true,
    last_date: '2023-09-15',
    created_at: '2023-07-21T11:40:00Z',
    updated_at: '2023-07-22T08:20:00Z',
    active: true,
    views_count: 90,
    click_count: 18,
    featured: true,
    paid: false,
    paid_amount: 0,
    paid_at: null,
    paid_until: null,
    phone_number: '111-222-3333',
    address: '123 Maple St, Chicago, IL',
    email: 'graphic@example.com',
    author: 'Emily Williams',
    openings: 2,
  },
]);




</script>  