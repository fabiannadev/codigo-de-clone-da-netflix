# codigo-de-clone-da-netflix
(ainda não esta concluido o projeto)
<h4> Estou criando um clone da netflix com reactjs </h4>
<h3> mostrarei a seguir o codigo que estou escrevendo:</h3>
<h2> app.js</h2>
<p>import React, {useEffect, useState} from 'react';
import Tmdb from './tmdb';
import namor from './src/namor';

const [movieList, setMovieList]= useState([]);
useEffect( () =>
  const loadAll= async () =>{
 let list= await Tmdb.getHomeList();
    setMovieList(list);
  }
          loadAll();
},[]);
  


export default () => {
  return (
    <div className="page">
      <section> 
      </section className="lists">
      {movieList.map((item, key) =>(
     <namor key={key} title={item.title} items={item.items}/>
      ))}
     
    </div>
  );
};
</p>
<h2>tmdb.js</h2>
<p>
  const API_KEY= "b65d2507a1d6c3b780ab57ca04d34338";
const API_BASE="https://api.themoviedb.org/3";
const basicFetch= async (endpoint) =>{
  const req= await fetch (`${API_BASE)$(endpoint`);
  const json= await req.json();
  return json;
}
export default{
  getHomeList: async () => {
    return [
    
      { slug: 'originals',
      title: 'originais da netflix',
      items await basicFetch(`/discover/tv?with_network=213&language=pt-br&api_key=${API_KEY}`)
      },
      {
       slug: 'trending'
      title: 'recomendados para você'
      items:await basicFetch(`/trending/all/week?language=pt-br&api_key=${API_KEY}`)
      },
      {
       slug: 'toprated'
      title: 'em alta'
      items:await basicFetch(`/movie/top_rated?language=pt-br&api_key=${API_KEY}`)
      },
    {
       slug: 'action'
      title: 'ação'
      items:await basicFetch(`/discover/movie?with_genres=28&language=pt-br&api_key=${API_KEY}`)
      },
      {
       slug: 'comedy'
      title: 'comedia'
      items:await basicFetch(`/discover/movie?with_genres=35&language=pt-br&api_key=${API_KEY}`)
      },
      {
       slug: 'horror'
      title: 'terror'
  </p>
  <h2>namor</h2>
  <p>
  import React from 'react';
import './namoral.css';


export default({title. items}) =>{
  return(
    <div> <h2>{title}</h2>
    </div>
    <div className="moviRow -- listarea">
    {items.results.lenght > 0 && items.results.map((item, key) => <img src={https://image.tmdb.org/t/p/w300${item.poster_path}`}/>
      
    ))}
    );

}
  </p>
  
  <p> Ainda não terminei, mas em breve, voltarei a atualizar o codigo e trazer mais informações do projeto. </p>
