import { createClient } from '@supabase/supabase-js'
const supabaseUrl = 'https://oswkovbecbfqqsftbmyq.supabase.co'
const supabaseKey = 'sb_publishable_wEu-hXDSdFhAnq21NIzv8A_Fqo45koY'
const supabase = createClient(supabaseUrl, supabaseKey)
async function obtenerEstudiantes() {
const { data, error } = await supabase
.from('Estudiantes')
.select('*')
if (error) {
console.log('Error:', error)
} else {
console.log('Datos:', data)
}
}
obtenerEstudiantes()
