<template>
  <synapseApp>
    <synapseHeader></synapseHeader>
    <synapseContent>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n"></synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn>Lorem ipsum dolor sit amet.</synapseColumn>
        <synapseColumn>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quas doloremque laborum odit repellendus modi illo omnis blanditiis? Ipsa iure deleniti labore quia autem rerum voluptatem, officiis natus minus impedit expedita rem nihil nesciunt doloremque id eveniet, ducimus voluptates et, reprehenderit quis! Sint, quam! Eos optio quas, omnis amet laborum tempore delectus cum non repudiandae, labore nostrum incidunt dolores, laboriosam vero asperiores maxime harum. Cum necessitatibus alias sequi cumque itaque quo voluptatum, omnis est molestiae quam maiores delectus placeat quisquam asperiores? Asperiores eos quam non consequatur? Corrupti ratione tempora quam consectetur! Maiores fugiat deleniti animi consectetur ipsum tenetur dolorem optio nostrum.</synapseColumn>
        <synapseColumn>Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio, neque.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti exercitationem cumque nulla. Molestiae, voluptate ipsum. Aliquid, culpa nisi earum illo tempora hic rem voluptatibus sequi totam ratione consectetur natus, consequuntur repudiandae sit magni velit libero ea repellendus doloribus molestias aliquam deleniti eligendi itaque ipsa. Repellendus natus et fuga illum culpa facilis similique quibusdam exercitationem non minima repellat doloremque, commodi impedit dolore cupiditate iusto nisi cum vitae, porro voluptatem? Provident suscipit sequi ex soluta voluptatem quis quod delectus tempora, labore facere. At soluta error velit aspernatur praesentium totam consequuntur dolor beatae, optio nobis sapiente! Voluptates veritatis obcaecati, nostrum tempore dolorum magni.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 12" :key="n">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eligendi pariatur eos maiores impedit ipsam voluptate rerum quae iure, voluptatem ea?</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 6" :key="n">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Obcaecati molestias voluptates cum recusandae. Molestias sunt molestiae dicta obcaecati tempore! Beatae hic ut voluptatum suscipit perspiciatis eveniet facilis accusamus id, harum, reiciendis itaque, delectus enim quo reprehenderit libero excepturi et? Exercitationem.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 24" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus reprehenderit, a modi eos est maxime eaque ex dicta quisquam sunt totam molestiae. Quidem, iusto quas. Pariatur autem maiores excepturi incidunt.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam, porro!</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 102" :key="n">Lorem, ipsum dolor.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus dolorum soluta quibusdam, tempore natus ipsum quo exercitationem placeat molestiae quos, libero inventore laboriosam tempora repudiandae maiores amet ea odit sint veniam non a aliquid, quisquam animi! Iusto ullam est accusantium in quos rerum delectus libero ducimus impedit. Nulla maxime fuga quos modi repudiandae distinctio? Saepe officia ut nisi quibusdam pariatur fuga ipsa sint, vel ipsum eius voluptate quasi optio odio aliquam incidunt. Sint laborum quasi tenetur nam! Adipisci iste dignissimos eum debitis dolorum, placeat corporis, fugiat, quos nam ab maiores libero esse eligendi aliquid error impedit voluptates distinctio ratione aperiam quae sequi architecto officiis earum consectetur. Neque, cupiditate est unde placeat earum obcaecati facere, doloribus error asperiores voluptatum, at dolores quibusdam? Qui illo nostrum natus animi quia ea laborum ex maiores esse, non laboriosam nihil facilis aliquid est, fugit expedita! Voluptatibus mollitia sed quasi nostrum quia aspernatur consequatur voluptate, facere nihil officia provident ea vel, necessitatibus consectetur molestiae alias quos commodi nulla reiciendis delectus iure quo earum! Laborum dolores aperiam earum voluptatibus quo eos, error blanditiis ipsum perferendis, perspiciatis ut recusandae. Accusamus dolores id quas quia repudiandae illo, aut reiciendis suscipit quis quos. Magni temporibus debitis, similique neque officia maiores.</synapseColumn>
      </synapseRow>
    </synapseContent>
    <synapseFooter></synapseFooter>
  </synapseApp>
  <!-- Next: add props to each component -->
</template>

<script>
import synapseApp from './components/synapseApp'
import synapseHeader from './components/synapseHeader'
import synapseContent from './components/synapseContent'
import synapseFooter from './components/synapseFooter'
import synapseRow from './components/synapseRow'
import synapseColumn from './components/synapseColumn'
export default {
  name: 'App',
  components: {
    synapseApp,
    synapseHeader,
    synapseContent,
    synapseFooter,
    synapseRow,
    synapseColumn
  }
}
</script>
